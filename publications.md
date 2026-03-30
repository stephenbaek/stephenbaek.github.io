---
layout: post
title: Publications
author: "stephenbaek"
permalink: /publications/
---

<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js@1.0.0/src/bibtex_js.min.js"></script>
<script>
    window.addEventListener('load', function() {
        const params = new URLSearchParams(location.search);
        const topic = params.get("topic");
        const author = params.get("author");
        const journal = params.get("journal");
        if(topic){
            if(topic=="materiq")
                document.getElementById("topic_search").value = 'microstructure|physics|dynamics|shock|materials|parc|superhydrophobic';
            if(topic=="design")
                document.getElementById("topic_search").value = 'manufacture|manufacturing|shape terra|topology optimization|asphalt';
        }
        // let countryInStorage = localStorage.getItem("country");

        // if (countryInStorage && !location.pathname.includes(countryInStorage)) {
        //     location.href = `/${PREFIX}/${countryInStorage}`;
    })
    let imageMap = {};

    fetch("/assets/publications/images.json")
        .then(res => res.json())
        .then(data => {
            imageMap = data;
        });
    function bibtex_callback(bibtex_display){
        // Count the total number of publicatiions within the category (for numbering)
        let pub_cnt = 0        
        for (let i = 0; i < bibtex_display.children.length; i++) {
            pub_cnt += bibtex_display.children[i].getElementsByClassName('bibtexentry').length;
        }
        // For each year
        for (let i = 0; i < bibtex_display.children.length; i++) {
            // Remove the entry if the current year publication is empty
            if(bibtex_display.children[i].getElementsByClassName('bibtexentry').length == 0){
                bibtex_display.children[i].remove();
                i--;
            }
            // Otherwise
            else{
                // Convert entries to lists
                let entries = bibtex_display.children[i].getElementsByClassName('bibtexentry')
                for(let j = 0; j < entries.length; j++){
                    //if(entries[j].getElementsByClassName('image').length){
                    //    var img = document.createElement("img");
                    //    img.src = "/assets/publications/" + entries[j].getElementsByClassName('image')[0].innerHTML;
                    //    entries[j].appendChild(img);
                    //    entries[j].getElementsByClassName('image')[0].parentElement.remove();
                    //    entries[j].style.paddingBottom = "50px"
                    //}
                    
                    let citekeyElem = entries[j].getElementsByClassName('citekey')[0];
                    let citekey = citekeyElem.getAttribute("id");

                    if (citekey && imageMap[citekey]) {
                        let img = document.createElement("img");
                        img.src = "/assets/publications/" + citekey + "." + imageMap[citekey];

                        img.style.width = "100%";
                        img.style.display = "block";
                        img.style.marginBottom = "75px";

                        entries[j].appendChild(img);
                    }

                    entries[j].innerHTML = "<li>" + entries[j].innerHTML + "</li>";
                }
                bibtex_display.children[i].getElementsByClassName('templates')[0].innerHTML = 
                    "<ol start = '" + pub_cnt.toString() + "' reversed='reversed'>" + bibtex_display.children[i].getElementsByClassName('templates')[0].innerHTML + "</ol>";
                pub_cnt = pub_cnt - bibtex_display.children[i].getElementsByClassName('bibtexentry').length;
            }
        }
    }
    function noyear_callback(bibtex_display){
        let entries = bibtex_display.getElementsByClassName('bibtexentry');
        for(let i = 0; i < entries.length; i++){
            if(entries[i].getElementsByClassName('howpublished').length == 0){
                entries[i].remove();
                i--;
            }
        }
        bibtex_callback(bibtex_display)
        let titles = bibtex_display.getElementsByTagName('h2');
        for(let i = 0; i < titles.length; i++){
            titles[i].remove();
            i--;
        }
    }
</script>

<!-- <bibtex src="test.bib"></bibtex>
<bibtex src="text1.bib"></bibtex> -->
<bibtex src="/assets/publications/publications.bib"></bibtex>
<div class="bibtex_structure">
  <div class="group year" extra="DESC number">
    <h2 class="title"></h2>
    <div class="templates"></div>
  </div>
</div>

<div class="bibtex_template">
    <span class="bibtexVar citekey" extra="BIBTEXKEY" id="+BIBTEXKEY+" style="display:none;"></span>
    <div style="font-weight: bold;">
        <span class="title"></span>
    </div>
    <div class="if author">
        <span class="author" max="10"></span>
    </div>
    <div class="if journal">
        <span class="journal" style="font-style: italic;"></span><span class="if volume">, <span class="volume"></span><span class="if number">(<span class="number"></span>)</span>:</span><span class="if pages"> <span class="pages"></span></span>.
    </div>
    <div class="if booktitle">
        <span class="booktitle" style="font-style: italic;"></span><span class="if address">, <span class="address"></span></span><span class="if pages">, <span class="pages"></span></span>.
    </div>
    <div class="if howpublished">
        <span class="howpublished"></span>
    </div>
    <div class="if doi">
        <a class="bibtexVar" href="http://dx.doi.org/+DOI+" extra="doi">
        https://dx.doi.org/<span class="doi"></span>
        </a>
    </div>
    <div class="if addendum">
        <span class="addendum" style="color:#E84A5F; font-weight: bold;"></span>
    </div>
    <!-- <div class="if image">
        <span class="image"></span>
    </div> -->
    <!-- <img class="bibtexVar" extra="BIBTEXKEY" id='+BIBTEXKEY+'> -->
    <!-- <img class="bibtexVar" src="/assets/publications/+BIBTEXKEY+.jpg" extra="BIBTEXKEY" onerror="imgError(this)"> -->
    <br/>
</div>
<!-- 
<input type="text" class="bibtex_search" id="searchbar" placeholder="Search publications"> -->


<div>
<div>
Filter Results: 
</div>
<div>
    <select class="bibtex_search bibtex_generate_author" search="author" style="width:30%; position: relative; float: left;" id="author_search">
    <option value="">All Coauthors</option>
    </select>
    <select class="bibtex_search" style="width:69%; margin-right: 0; position: relative; float: right;" id="topic_search">
    <option value="">All Topics</option>
    <!-- Add topic values here -->
    <option value="award|featured in|best|hottest">Awarded</option>
    <option value="microstructure|physics|dynamics|shock|materials|parc|superhydrophobic">Materials Science & Engineering</option>
    <option value="manufacture|manufacturing|shape terra|topology optimization|asphalt">Computational Design and Engineering</option>
    <option value="zernet|topology graph|spectral descriptors|curvature flow|differential operator|isometric shape|surface normal|volume drawing|gafinc|surface registration|mesh segmentation|lego|geodesic|point cloud|kinecad|RBF network">Computational Geometry</option>
    <option value="body shape|pose estimation|body surface|human body|anatomical|knee|vertebra|handheld|foot|insole|femur|fall-risk|ergonomic|worker|body scan|human model">Digital Human Modeling</option>
    <option value="tumor|anmaf|cancer|cardiac|aneurysm|tomography|neocortex|cotransport|radiotherapy|dental|radiography|c-arm|synthetic ct">Medical Imaging</option>
    <option value="economic|shape matters">Social Science</option>
    <option value="federated learning|extreme learning machine|copula|index theory|geometric data|elmvis">Machine Learning Foundations</option>
    </select>
    <select class="bibtex_search bibtex_generate_journal" search="journal" style="width:100%" id="journal_search">
    <option value="">All Journals</option>
    </select>
</div>
</div>


# Working Papers
<div class="bibtex_display" bibtextypekey="MISC" callback="noyear_callback(bibtex_display)"></div>
<br/>&nbsp;<br/>


# Journal Publications
<div class="bibtex_display" bibtextypekey="ARTICLE" callback="bibtex_callback(bibtex_display)"></div>

<br/>&nbsp;<br/>

# Conference and Workshop Papers
<div class="bibtex_display" bibtextypekey="INPROCEEDINGS" callback="bibtex_callback(bibtex_display)"></div>


