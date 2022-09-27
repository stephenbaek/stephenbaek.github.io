---
layout: post
title: Publications
author: "stephenbaek"
permalink: /publications/
---

<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js@1.0.0/src/bibtex_js.min.js"></script>
<script>
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
                    if(entries[j].getElementsByClassName('image').length){
                        var img = document.createElement("img");
                        img.src = "/assets/publications/" + entries[j].getElementsByClassName('image')[0].innerHTML;
                        entries[j].appendChild(img);
                        entries[j].getElementsByClassName('image')[0].parentElement.remove();
                        entries[j].style.paddingBottom = "50px"
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
    <div class="if image">
        <span class="image"></span>
    </div>
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
    <select class="bibtex_search bibtex_generate_author" search="author" style="width:30%; position: relative; float: left;">
    <option value="">All Coauthors</option>
    </select>
    <select class="bibtex_search" style="width:69%; margin-right: 0; position: relative; float: right;">
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
    <select class="bibtex_search bibtex_generate_journal" search="journal" style="width:100%">
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




<!-- 
# Working Papers

0. **Federated learning on adaptively weighted nodes by bilevel optimization**<br/>
Huang, Y., Lin, Q., Baek, S., & Street, N.<br/>
[arXiv:2207.10751](https://arxiv.org/abs/2207.10751)

0. **Physics-aware recurrent convolutional (PARC) neural networks to assimilate meso-scale reactive mechanics of energetic materials**<br/>
Nguyen, P. C., Nguyen, Y.-T., Choi, J. B., Seshadri, P. K., Udaykumar, H., & Baek, S.<br/>
[arXiv:2204.07234](https://arxiv.org/abs/2204.07234)

0. **A predictive model using a deep segmentation network for acute coronary events (ACE) after breast radiotherapy**<br/>
Choi, B. S., Yoo, S. K., Moon, J., Chung, S. Y., Oh, J., Baek, S., Kim, Y., Chang, J. S., Kim, H., & Kim, J. S.<br/>

0. **On the role of depth predictions for 3d human pose estimation**<br/>
Diaz-Arias, A., Messmore, M., Shin, D., & Baek, S.<br/>
[arXiv:2103.02521](https://arxiv.org/abs/2103.02521)

0. **Interpretable sequence classification via prototype trajectory**<br/>
Hong, D., Baek, S., & Wang, T.<br/>
[arXiv:2007.01777](https://arxiv/org/abs/2007.01777)
{:start="5"}
{:reversed="reversed"} 

<br/>&nbsp;

# Journal Publications
### 2022
0. **Synthesizing controlled microstructures of porous media using generative adversarial networks and reinforcement learning**<br/>
Nguyen, P. C., Vlassis, N. N., Bahmani, B., Sun, W., Udaykumar, H., & Baek, S.<br/>
*Scientific Reports*,<br/>
[doi:10.1038/s41598-022-12845-7](https://doi.org/10.1038/s41598-022-12845-7)<br/>
![](/assets/publications/nguyen2022ganac.png)<br/>&nbsp;

0. **Enabling AI innovation via data and model sharing: an overview of the NSF Convergence Accelerator Track D**<br/>
Baru, C., Pozmantier, M., Altintas, I., Baek, S., Cohen, J., Condon, L., Fanti, G., Fernandez, R. C., Jackson, E., Lall, U., Landman, B., Li, H. H., Marin, C., Lopez, B. M., Metaxas, D., Olsen, B., Page, G., Shang, J., Turkan, Y., & Zhang, P.<br/>
*AAAI AI Magazine*,<br/>
[doi:10.1002/aaai.12042](https://doi.org/10.1002/aaai.12042)<br/>

0. **Meso-scale simulation of energetic materials I: a method for generating synthetic microstructures using deep feature representations**<br/>
Roy, S., Neal, C., Nguyen, Y. T., Baek, S., & Udaykumar, H. S.<br/>
*Journal of Applied Physics*,<br/>
[doi:10.1063/5.0065294](https://doi.org/10.1063/5.0065294)<br/>
{:start="36"}
{:reversed="reversed"}

### 2021
0. **Machine learning model for understanding laser superhydrophobic surface functionalization**<br/>
Huang, W., Samanta, A., Chen, Y., Baek, S., Shaw, S. K., & Ding, H.<br/>
*Journal of Manufacturing Processes*,<br/>
[doi:10.1016/j.jmapro.2021.08.007](https://doi.org/10.1016/j.jmapro.2021.08.007)<br/>

0. **Body shape matters: Evidence from machine learning on body shape-income relationship**<br/>
Song, S. & Baek, S.<br/>
*PLOS ONE*,<br/>
[doi:10.1371/journal.pone.0254785](https://doi.org/10.1371/journal.pone.0254785)<br/>
(<span style="color:#E84A5F">**Featured in PsyPost, Daily Mail, CBS The Doctors TV Show, Virginia Public Radio, and others**</span>)
![](/projects/shape-matters/img/graphAE.png)<br/>&nbsp;

0. **Machine learning prediction of fall-risk in older adults using timed up & go test kinematics**<br/>
Roshdibenam, V., Jogerst, G. J., Butler, N. R., & Baek, S.<br/>
*Sensors*,<br/>
[doi:10.3390/s21103481](https://doi.org/10.3390/s21103481)<br/>

0. **ANMAF: an automated neuronal morphology analysis framework using convolutional neural networks**<br/>
Tong, L., Langton, R., Glykys, J., & Baek, S.<br/>
*Scientific Reports,*<br/>
[doi:10.1038/s41598-021-87471-w](https://doi.org/10.1038/s41598-021-87471-w)
{:start="33"}
{:reversed="reversed"}

### 2020
0. **Mesh repairing using topology graphs**<br/>
Charton, J., Baek, S., & Kim, Y.<br/>
*Journal of Computational Design and Engineering*, <br/>
[doi:10.1093/jcde/qwaa076](https://doi.org/10.1093/jcde/qwaa076)<br/>
![](/assets/publications/charton2020.jpg)<br/>&nbsp;

0. **Deep learning for synthetic microstructure generation in a materials-by-design framework for heterogeneous energeticmaterials**<br/>
Chun, S., Roy, S., Nguyen, Y. T., Choi, J. B., Udaykumar, H., & **Baek, S.**<br/>
*Scientific Reports*, 10: 13307<br/>
[doi:10.1038/s41598-020-70149-0](https://doi.org/10.1038/s41598-020-70149-0)<br/>
[Nature Research Community Blog](https://devicematerialscommunity.nature.com/posts/generating-synthetic-material-microstructures-using-generative-adversarial-networks-gan)<br/>
![](/assets/publications/chun2020gan.gif)<br/>&nbsp;

0. **ZerNet: Convolutional neural networkson arbitrary surfaces via Zernike local tangent space estimation**<br/>
Sun, Z., Rooke, E., Charton, J., He, Y., Lu, J., & **Baek, S.**<br/>
*Computer Graphics Forum*, 39(6): 204-216<br/>
[doi:10.111/cgf.14012](https://doi.org/10.1111/cgf.14012)<br/>
![](/assets/publications/sun2020zernet.png)<br/>&nbsp;

0. **Embedded spectral descriptors: learning the point-wise correspondence metric via Siamese neural networks**<br/>
Sun, Z., He, Y., Gritsenko, A., Lendasse, A., & **Baek, S.**<br/>
*Journal of Computational Design and Engineering*, 7(1): 18–29<br/>
[doi:10.1093/jcde/qwaa003](https://doi.org/10.1093/jcde/qwaa003)<br/>
![](/assets/publications/sun2020siamese.png)<br/>&nbsp;
{:start="29"}
{:reversed="reversed"}

### 2019
0. **Deep segmentation networks predict survival of non-small cell lung cancer**<br/>
**Baek, S.**, He, Y. (equal contribution), Allen, B. G., Buatti, J. M., Smith, B. J., Tong, L., Sun, Z., Li, R., Wu, J., Diehn, M., Loo, B. W., Plichta, K. A., Seyedin, S. N., Gannon, M., Cabel, K. R., Kim, Y., & Wu, X.<br/>
*Scientific Reports*, 9: 17286<br/>
[doi:10.1038/s41598-019-53461-2](https://doi.org/10.1038/s41598-019-53461-2)<br/>
![](/assets/publications/he2019cancer.png)<br/>&nbsp;

0. **Modeling and forecasting short-term power load with copula model and deep belief network**<br/>
Ouyang, T., He, Y., Li, H., Sun, Z., & **Baek, S.**<br/>
*IEEE Transactions on Emerging Topics in Computational Intelligence*, 3(2): 127-136<br/>
[doi:10.1109/TETCI.2018.2880511](https://doi.org/10.1109/TETCI.2018.2880511)

0. **4D cardiac motion modeling using pair-wise mesh registration**<br/>
Yoon, S., **Baek, S.**, & Lee, D.<br/>
*Lecture Notes in Computer Science*, 11395: 161–170<br/>
[doi:10.1007/978-3-030-12029-0_18](https://doi.org/10.1007/978-3-030-12029-0_18)
{:start="25"}
{:reversed="reversed"}

### 2018

0. **A quantitative assessment of variations in the palm surface area as a percentage of total body surface area within the general population**<br/>
Liu, T. C., Bhatt, R., Farrell, K. D., **Baek, S.**, Liu, Y. M., Abdel-Malek, K., & Arora, J.<br/>
*International Journal of Human Factors Modelling and Simulation*, 6(1): 81–96<br/>
[doi:10.1504/IJHFMS.2018.091359](https://doi.org/10.1504/IJHFMS.2018.091359)

0. **Extreme Learning Machinesfor VISualization+R - Mastering visualization with target variables**<br/>
Gritsenko, A., Akusok, A., **Baek, S.**, Miche, Y., & Lendasse, A.<br/>
*Cognitive Computation*, 10(3): 464–477<br/>
[doi:10.1007/s12559-017-9537-6](https://doi.org/10.1007/s12559-017-9537-6)<br/>
![](/assets/publications/Gritsenko2018.jpg)<br/>&nbsp;

0. **Manufacturability analysis for additive manufacturing using a novel feature recognition technique**<br/>
Shi, Y., Zhang, Y., **Baek, S.**, Backer, W. D., & Harik, R.<br/>
*Computer-Aided Design and Applications*, 15(6): 941-952<br/>
[doi:10.1080/16864360.2018.1462574](https://doi.org/10.1080/16864360.2018.1462574)<br/>
![](/assets/publications/Shi2018.jpg)<br/>&nbsp;

0. **Machine learning-aided exploration of relationship between strength and elastic properties in ascending thoracic aneurysm**<br/>
Luo, Y., Fan, Z., **Baek, S.**, & Lu, J.<br/>
*International Journal for Numerical Methods in Biomedical Engineering*, 34(6): e2977<br/>
[doi:10.1002/cnm.2977](https://doi.org/10.1002/cnm.2977)

0. **Mesh segmentation via geodesic curvature flow**<br/>
Sun, Z., Harik, R., & **Baek, S.**<br/>
*Computer-Aided Design and Applications*, 15(5): 677–683<br/>
[doi:10.1080/16864360.2018.1441235](https://doi.org/10.1080/16864360.2018.1441235)<br/>
![](/assets/publications/Sun2018.jpg)<br/>&nbsp;
{:start="22"}
{:reversed="reversed"}

### 2017

0. **Shape Terra: mechanical feature recognition based on a persistent heat signature**<br/>
Harik, R., Shi, Y., & **Baek, S.**<br/>
*Computer-Aided Design and Applications*, 14(2): 206–218<br/>
[doi:10.1080/16864360.2016.1223433](https://doi.org/10.1080/16864360.2016.1223433)<br/>
![](/assets/publications/Harik2017.jpg)<br/>&nbsp;
{:start="17"}
{: reversed="reversed"}

### 2016
0. **ELMVIS+: Fast nonlinear visualization technique based on cosine distance and extreme learning machines**<br/>
Akusok, A., **Baek, S.**, Miche, Y., Björk, K.-M., Nian, R., Lauren, P., & Lendasse, A.<br/>
*Neurocomputing*, 205: 247–263<br/>
[doi:10.1016/j.neucom.2016.04.039](https://doi.org/10.1016/j.neucom.2016.04.039)<br/>
![](/assets/publications/Akusok2016a.jpg)<br/>&nbsp;

0. **Statistical foot shape analysis for mass-customisation of footwear**<br/>
**Baek, S.-Y.** & Lee, K.<br/>
*International Journal of Computer Aided Engineering and Technology*, 8(1/2): 80–98<br/>
[doi:10.1504/IJCAET.2016.073265](https://doi.org/10.1504/IJCAET.2016.073265)
<br/>&nbsp;
{:start="16"}
{: reversed="reversed"}

### 2015
0. **Differential operators on a triangular mesh and their applications**<br/>
**Baek, S.-Y.**, Kam, D.-U., & Lee, K.<br/>
*Transactions of the Society of CAD/CAM Engineers*, 20(1): 44–54.<br/>
![](/assets/publications/Baek2015b.jpg)<br/>&nbsp;

0. **Isometric shape interpolation**<br/>
Baek, S.-Y., Lim, J., & Lee, K.<br/>
*Computers & Graphics*, 46(1): 257–263<br/>
[doi:10.1016/j.cag.2014.09.025](https://doi.org/10.1016/j.cag.2014.09.025)<br/>
<img src="/assets/GitHub-Mark-20px.png" style="display:inline;margin: 0 0 -4px 0;"> [Source Code](https://github.com/stephenbaek/isoblend)<br/>
![](/assets/publications/Baek2015a.jpg)<br/>&nbsp;

0. **An algorithm for estimating surface normal from its boundary curves**<br/>
Park, J., Kim, T., **Baek, S.-Y.**, & Lee, K.<br/>
*Journal of Computational Design and Engineering*, 2(1): 67–72<br/>
[doi:10.1016/j.jcde.2014.11.007](https://doi.org/10.1016/j.jcde.2014.11.007)<br/>
![](/assets/publications/Park2015.jpg)<br/>&nbsp;
{:start="14"}
{: reversed="reversed"}

### 2014
0. **An isometric shape interpolation method on mesh models**<br/>
**Baek, S.-Y.** & Lee, K.<br/>
*Transactionsof the Society of CAD/CAM Engineers*, 19(2): 1–10

0. **3D volume drawing on a potter’s wheel**<br/>
Cho, S., Baek, D., **Baek, S.-Y.**, Lee, K., & Bang, H.<br/>
*IEEE Computer Graphics and Applications*, 34(3): 50–58<br/>
[doi:10.1109/MCG.2014.3](https://doi.org/10.1109/MCG.2014.3)<br/>
<img src="/assets/youtube-20x20.png" style="display:inline;margin: 0 0 -4px 0;"> [Video](https://www.youtube.com/watch?v=zbYn-kwfMlc)<br/>
![](/assets/publications/Cho2014.jpg)<br/>&nbsp;

0. **Automatic detection of inferior alveolar nerve canal from cone-beam computed tomography images for dental surgery planning**<br/>
Choi, J.-H., **Baek, S.-Y.**, Kim, Y., Son, T.-G., Park, S., & Lee, K.<br/>
*Studies in Health Technology and Informatics*, 196(1): 61–65<br/>
[doi:10.3233/978-1-61499-375-9-61](https://doi.org/10.3233/978-1-61499-375-9-61)

0. **GaFinC: gaze and finger control interface for 3D model manipulation in CAD application**<br/>
Song, J., Cho, S., **Baek, S.-Y.**, Lee, K., & Bang, H.<br/>
*Computer-Aided Design*, 46(1): 239–245<br/>
[doi:10.1016/j.cad.2013.08.039](https://doi.org/10.1016/j.cad.2013.08.039)<br/>
<img src="/assets/youtube-20x20.png" style="display:inline;margin: 0 0 -4px 0;"> [Video](https://www.youtube.com/watch?v=TTwwV7xc_Aw)<br/>
![](/assets/publications/Song2014.jpg)<br/>&nbsp;
{:start="11"}
{: reversed="reversed"}

### 2013
0. **Parametric human body modeling system for virtual garment fitting**<br/>
**Baek, S.-Y.** & Lee, K.<br/>
*International Journal of Computer Aided Engineering and Technology, 5(2/3): 242–261<br/>
[doi:10.1504/IJCAET.2013.052932](https://doi.org/10.1504/IJCAET.2013.052932)

0. **Automated bone landmarks prediction on the femur using anatomical deformation technique**<br/>
**Baek, S.-Y.**, Wang, J. H., Song, I., Lee, K., Lee, J., & Koo, S.<br/>
*Computer-Aided Design*, 45(2): 505–510<br/>
[doi:10.1016/j.cad.2012.10.033](https://doi.org/10.1016/j.cad.2012.10.033)<br/>
![](/assets/publications/Baek2013a.jpg)<br/>&nbsp;
{:start="7"}
{: reversed="reversed"}

### 2012
0. **Changes in medio-lateral knee joint reactionforce of patients with over-pronation during gait due to insole parameters - A case study**<br/>
Lee, S., **Baek, S.-Y.**, Son, J., Kim, D., & Lee, K.<br/>
*Transactionsof the Society of CAD/CAM Engineers*, 17(3): 149–155

0. **Parametric human body shape modeling framework for human-centered product design**<br/>
**Baek, S.-Y.** & Lee, K.<br/>
*Computer-Aided Design*, 44(1): 56–67<br/>
[doi:10.1016/j.cad.2010.12.006](https://doi.org/10.1016/j.cad.2010.12.006)<br/>
**Top 25 Hottest Articles Published in Computer-Aided Design in 2012, Elsevier**<br/>
![](/assets/publications/Baek2012.jpg)<br/>&nbsp;
{:start="5"}
{: reversed="reversed"}

### 2010
0. **3D generic vertebra model for computer aided diagnosis**<br/>
Lee, J., **Baek, S.-Y.**, & Lee, K.<br/>
*Transactions of the Society of CAD/CAM Engineers*, 15(4): 297–305<br/>
**Best Paper of the Year**

0. **Evaluation of handheld products by computinguser hand fatigue**<br/>
Choi, J.-H., Park, S.-W., **Baek, S.-Y.**, & Lee, K.<br/>
*Simulation Modeling Practice and Theory*, 18(2): 230–239<br/>
[doi:10.1016/j.simpat.2009.10.009](https://doi.org/10.1016/j.simpat.2009.10.009)<br/>
![](/assets/publications/Choi2010.jpg)<br/>&nbsp;
{:start="3"}
{: reversed="reversed"}

### 2009
0. **Synthesis of human body shape for given body sizes using 3D body scan data**<br/>
Jang, T., **Baek, S.-Y.**, & Lee, K.<br/>
*Transactions of the Society of CAD/CAM Engineers*, 14(6): 364–373<br/>
**Best Paper of the Year**
{: reversed="reversed"}

<br/>&nbsp;

# Conference Presentations

### 2022
0. **Cation-chloride cotransporters' role in neuronal swelling during oxygen-glucose deprivation in the neonatal neocortex.**
Takezawa, Y., Langton, R., Baule, S. M., Zimmerman, M. B., Baek, S., & Glykys, J.<br/>
In *The Society for Neuroscience 2022 Annual Meeting. San Diego, California. To appear.*

0. **A deep learning approach for topology optimization to enhance structural design**
Moghadasi, N., Nguyen, P. C., & Baek, S.<br/>
In *ASME International Mechanical Engineering Congress & Exposition (IMECE). Columbus, Ohio. To appear.*

0. **Multiscale homogenization for structure-property linkage modeling in design for additive manufacturing of cellular structure**
Nguyen, P. C., Kim, Y., Choi, Y., & Baek, S.<br/>
In *ASME International Mechanical Engineering Congress & Exposition (IMECE). Columbus, Ohio. To appear.*

0. **Physics-aware AI-directed framework for microstructural design of shocked materials**
Choi, J., Nguyen, P., Nguyen, Y.-T., Udaykumar, H., & Baek, S.<br/>
*In The USACM Thematic Conference on Uncertainty Quantification for Machine Learning Integrated Physics Modeling (MLIP). Arlington, Virginia.*
(<span style="color:#E84A5F">**Best Poster Award**</span>)

0. **A novel AI-assisted framework for microstructural design of shocked materials**
Choi, J. B., Nguyen, P. C., Nguyen, Y.-T., Udaykumar, H., & Baek, S.<br/>
In *The 22nd Biennial Conference of the APS Topical Group on Shock Compression of Condensed Matter (SHOCK22). Anaheim, California.*

0. **Establishing the structure-property-performance linkage of pressed energetic materials using physics-aware recurrent convolutional neural networks (PARC)**
Nguyen, P. C. H., Choi, J. B., Nguyen, Y.-T., Udaykumar, H., & Baek, S.<br/>
In *The 22nd Biennial Conference of the APS Topical Group on Shock Compression of Condensed Matter (SHOCK22). Anaheim, California.*

0. **Learning continuum strength models for meso-scale simulations of HMX from molecular dynamics using deep neural networks**
Walters, D., Herrin, J., Sewell, T., Baek, S., & Udaykumar, H.<br/>
In *The 22nd Biennial Conference of the APS Topical Group on Shock Compression of Condensed Matter (SHOCK22). Anaheim, California.*

0. **Bridging meso- and macro-scales using machine learning for simulations of shocked heterogenous energetic materials**
Udaykumar, H., Baek, S., Nguyen, Y. T., Nguyen, P., & Sen, O.<br/>
In *The 19th U.S. National Congress on Theoretical and Applied Mechanics. Austin, Texas.*

0. **Exploring the structure-property-performance linkage of energetic materials via physics-aware recurrent convolutions**
Nguyen, P., Choi, J., Nguyen, Y.-T., Baek, S., & Udaykumar, H.<br/>
In *The Mach Conference. Baltimore, Maryland.*

0. **Synthesizing realistic images of material microstructures using convolutional neural networks**
Baek, S., Udaykumar, H., Sun, W., & Nguyen, P.<br/>
In *The 150th Annual Meeting & Exhibition of the Minerals, Metals & Materials Society (TMS2022). Anaheim, California.*
{:start="71"}
{: reversed="reversed"}

### 2021
0. Brown, C. R., Juno, J. L., Howes, G. G., Haggerty, C. C., Baek, S. S., & Batabyal, A. (2021). Anal-
ysis of instabilities in quasi-perpendicular magnetized collisionless shocks using the field-particle
correlation technique. In The 63th Annual Meeting of the APS Division of Plasma Physics.
{:start="61"}
{: reversed="reversed"}

### 2020
0. **Artificial intelligence techniques for materials-by-design of energetic materials**<br/>
Udaykumar, H. S., Baek, S., Nguyen, Y. T., Chun, S., & Seshadri, P. K.<br/>
In *The 32nd Joint Army Navy NASA Air Force (JANNAF) Energetics Systems Hazards (ESHS) Meeting. Virtual*

0. **The  use  of  machine  learning  topredict fall risk in older adults**<br/>
Jogerst, G., Roshdibenam, V., Butler, N., Xu, Y., & **Baek, S.**<br/>
In *North American Primary Care Research Group (NAPCRG) 48th Annual Meeting. San Francisco, California*

0. **Learning geometric data via generative neural networks**<br/>
**Baek, S.**<br/>
In *IISE Annual Conference & Expo 2020. New Orleans, Louisiana*

0. **Ergonomic assessment via deepconvolutional neural networks**<br/>
Shull, J. R., Kim, H., Roshdibenam, V., Fethke, N., & **Baek, S.**<br/>
In *IISE Annual Conference & Expo 2020. New Orleans, Louisiana*
{:start="60"}
{: reversed="reversed"}

### 2019
0. **NADS-Net: A nimble architecture for driver and seat belt detection via convolutional neural networks**<br/>
Chun, S., Hamidi Ghalehjegh, N., Choi, J. B., Schwarz, C. W., Gaspar, J. G., McGehee, D. V., **Baek, S.**<br/>
In *International Conference on Computer Vision (ICCV)-Autonomous Driving Workshop. Seoul, Korea*<br/>
(<span style="color:#E84A5F">**Acceptance rate:30.91%**</span>)
![](/assets/publications/chun2019nadsnet.png)<br/>&nbsp;

0. **Cotransport of water and chloride through co-cotransporters during neocortical seizures**<br/>
Duquette, E., Rahmati, N., Duquette, K., Tong, L., **Baek, S.**, Staley, K., & Glykys, J.<br/>
In *Gordon Research Conference: Spatio-Temporal Control of GABAergic Signaling and Its Breakdown in Brain Disorders. Newry, Maine, United States*

0. **Asphalt pavement crack detection based on deep learning**<br/>
Moon, B., Choi, J. B., Lee, H. D., & **Baek, S.**<br/>
In *International Conference on Smart Cities. Seoul, Korea*

0. **Synthetic CT generation using unpaired images in a CycleGAN with identity loss**<br/>
Sun, Z., **Baek, S.**, Yaddanapudi, S., & St-Aubin, J.<br/>
In *2019 Annual Meeting of the American Association of Physicists in Medicine (AAPM 2019), San Antonio, Texas*

0.  **Multi-scale embedded CNN for music tagging (MsE-CNN)**<br/>
Ghalehjegh, N. H., Vahidzadeh, M., & **Baek, S.**<br/>
In *International Conference on Machine Learning (ICML) Workshop. Long Beach, California, United States*
{:start="56"}
{: reversed="reversed"}
 
### 2018
0. **Shape matters: Evidences from machine learning on body shape-income relationship**<br/>
**Baek, S.** & Song, S.<br/>
In *88th Southern Economic Association Annual Meetings (SEA2018), Washington, D.C., United States*
 
0. **Shape matters: Evidences from machine learning on body shape-income relationship**<br/>
**Baek, S.** & Song, S.<br/>
In *28th Annual Meeting of Midwest Econometrics Group (MEG2018), Madison, Wisconsin, United States*

0. **4D cardiac motion modeling using pair-wise mesh registration**<br/>
Yoon, S., **Baek, S.**, & Lee, D.<br/>
In *21st International Conference on Medical Image Computing & Computer Assisted Intervention (MICCAI) Workshop, Granada, Spain*

0. **Economic models with non-Euclidean data**<br/>
**Baek, S.** & Song, S.<br/>
In *2018 Joint Statistical Meetings (JSM2018), Vancouver, Canada*

0. **Applying machine learning for automated liver segmentation on radiotherapy planning CT**<br/>
**Baek, S.**, Sun, Z., Yaddanapudi, S., Kim, Y., Gross, B., Hawkes, K., McCune, K., Yuan, T., & Xia, J.<br/>
In *2018 Annual Meeting of the American Association of Physicists in Medicine (AAPM2018), Nashville, Tennessee, United States*

0. **Predicting manufactured shapes of a projection micro-stereolithography process via convolutional encoder-decoder networks**<br/>
He, Y., Fei, F., Wang, W., Song, X., Sun, Z., & **Baek, S.**<br/>
In *ASME 2018 International Design Engineering Technical Conferences & Computers and Information in Engineering Conference (IDETC/CIE2018), Quebec, Canada*

0. **Wall stress estimation in cerebral aneurysm via geometric convolutional neural network**<br/>
**Baek, S.**, Sun, Z., & Lu, J.<br/>
In *8th World Congress of Biomechanics (WCB2018), Dublin, Ireland*

0. **Machine-learning investigation of relationship between strength and response features in ascending thoracic aneurysm tissue**<br/>
Luo, Y., Fan, Z., **Baek, S.**, & Lu, J.<br/>
In *8th World Congress of Biomechanics (WCB2018), Dublin, Ireland*

0. **Estimation of economic models with non-Euclidean data**<br/>
**Baek, S.** & Song, S.<br/>
In *New Frontiers in Econometrics, Stamford, Connecticut*
{:start="51"}
{: reversed="reversed"}

<br/>&nbsp;

### 2017
0. **Deformable surface registration with extreme learning machines**<br/>
Gritsenko, A., Sun, Z., **Baek, S.**, Miche, Y., Hu, R., & Lendasse, A.<br/>
In *International Conference on Extreme Learning Machines (ELM2017), Yantai, China*

0. **Mosquito Popper: A multiplayer online game for 3D body scan data segmentation**<br/>
Nolte, Z., Riley, M., Harik, R., & **Baek, S.**<br/>
In *14th Annual International CAD Conference (CAD’17), Okayama, Japan*

0. **Validation of feature recognition on manufacturability analysis for additive manufacturing**<br/>
Shi, Y., Zhang, Y., **Baek, S.**, & Harik, R.<br/>
In *14th Annual International CAD Conference (CAD’17), Okayama, Japan*

0. **Mesh segmentation via geodesic curvature flow**<br/>
Sun, Z., **Baek, S.**, & Harik, R.<br/>
In *14th Annual International CAD Conference (CAD’17), Okayama, Japan*

0. **Parametric modeling of Korean construction workers for the safer construction environment**<br/>
**Baek, S.**, Lee, H., Bhatt, R., Farrell, K., Arora, J. S., & Abdel-Malek, K.<br/>
In *International Conferenceon Maintenance and Rehabilitation of Constructed Infrastructure Facilities (2017MAIREINFRA), Seoul, Korea*<br/>
<span style="color:#E84A5F">**Best Paper Award**

0. **Classifying stress strain curves obtained at rupture and non-rupture sites in ascending thoractic aneurysm tissue using machine learning**<br/>
Luo, Y., **Baek, S.**, & Lu, J.<br/>
In *5th International Conference on Computational and Mathematical Biomedical Engineering (CMBE2017), Pittsburgh, PA, United States*
{:start="42"}
{: reversed="reversed"}

<br/>&nbsp;

### 2016
0. **Incremental ELMVIS for unsupervised learning**<br/>
Akusok, A., Eirola, E., Miche, Y., Oliver, I., Björk, K.-M., Gritsenko, A., **Baek, S.**, & Lendasse, A.<br/>
In *International Conference on Extreme Learning Machines (ELM2016), Marina Bay Sands, Singapore*

0. **ELMVIS++R – Mastering visualization with target variables**<br/>
Gritsenko, A., Akusok, A., **Baek, S.**, & Lendasse, A.<br/>
In *International Conference on Extreme Learning Machines (ELM2016), Marina Bay Sands, Singapore*

0. **Combined non-linear visualization and classification: ELMVIS++C**<br/>
Gritsenko, A., Akusok, A., Miche, Y., Bjork, K.-M., **Baek, S.**, & Lendasse, A.<br/>
In *2016 International Joint Conference on Neural Networks (IJCNN2016), Vancouver, Canada*<br/>
(<span style="color:#E84A5F">**Acceptance rate:58.33%**</span>)

0. **Development of full-resolution anthropometric human models based on nonlinear statistical shape analysis**<br/>
**Baek, S.**, Sun, Z., & Mate, S. S.<br/>
In *7th International Conference of Applied Human Factorsand Ergonomics, Orlando, Florida, United States*
{:start="36"}
{: reversed="reversed"}

<br/>&nbsp;

### 2015
0. **SHAPE TERRA: Industrial feature recognition based on persistent heat signature**<br/>
Harik, R., **Baek, S.-Y.**, Bruchem, B.-J. V., & Tooren, M. V.<br/>
In *12th Annual International CAD Conference (CAD’15), London, The United Kingdom*

0. **Shape Terra: A feature recognition tool using persistent heat signature**<br/>
Harik, R., **Baek, S.-Y.**, Bruchem, B.-J. V., & Tooren, M. V.<br/>
In *2015 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*
{:start="32"}
{: reversed="reversed"}

<br/>&nbsp;

### 2014
0. **Automatic generation of LEGO layout from 3D model**<br/>
Jang, S., Woo, S., Kam, D.-U., **Baek, S.-Y.**, & Lee, K.<br/>
In *2014 Autumn Conference of the Korean Society of Mechanical Engineers, Gwangju, Korea*<br/>
![](/assets/publications/Jang2014.jpg)<br/>&nbsp;

0. **Local parameterization of meshes using geodesics**<br/>
Kim, D.-W., **Baek, S.-Y.**, & Lee, K.<br/>
In *2014 Autumn Conference of the Korean Society of Mechanical Engineers, Gwangju, Korea*

0. **Extraction of a margin line for dental CAD**<br/>
Lee, J., Lim, J., **Baek, S.-Y.**, & Lee, K.<br/>
In *2014 Autumn Conference of the Korean Society of Mechanical Engineers, Gwangju, Korea*

0. **Optimization method for rapid rigid registration between X-ray and digitally reconstructed radiography**<br/>
Woo, S., **Baek, S.-Y.**, & Lee, K.<br/>
In *2014 Autumn Conference of the Korean Society of Mechanical Engineers, Gwangju, Korea*

0. **Isometric shape interpolation**<br/>
**Baek, S.-Y.**, Lim, J., & Lee, K.<br/>
In *Shape Modeling International (SMI2014), Hong Kong*<br/>
(<span style="color:#E84A5F">**Acceptance rate:36%**</span>)

0. **Differential operators on a triangular mesh and their applications**<br/>
**Baek, S.-Y.**, Kam, D.-U., & Lee, K.<br/>
In *2014 Summer Conference of the Society of CAD/CAM Engineers, Muju, Korea*<br/>
<span style="color:#E84A5F">**Best Paper Award**</span>

0. **Algorithm for generating high-precision pointcloud using quaternary coded structured light and phase**<br/>
Kim, D.-W., Lee, J., **Baek, S.-Y.**, & Lee, K.<br/>
In *2014 Summer Conference of the Society of CAD/CAM Engineers, Muju, Korea*

0. **Automatic generation of high-quality digitally reconstructed radiography for registration between 2D X-ray image and 3D CT image**<br/>
Woo, S., Lee, J.-H., **Baek, S.-Y.**, & Lee, K.<br/>
In *2014 Summer Conference of the Society of CAD/CAM Engineers, Muju, Korea*

0. **A C-arm calibration method for 2D-3D registration**<br/>
Lee, J.-H., Woo, S., **Baek, S.-Y.**, Lee, K., Dong, Y., & Lee, S.<br/>
In *2014 Annual Conference of the Korean Society of Medical Robot, Seoul, Korea*

0. **Automatic determination of the insertion axis of a dental crown that minimizes undercut area**<br/>
Lim, J., **Baek, S.-Y.**, Lee, J., & Lee, K.<br/>
In *10th International Symposium on Tools and Methods for Competitive Engineering (TMCE2014), Budapest, Hungary*

0. **An isometric shape nterpolation method on mesh models**<br/>
**Baek, S.-Y.** & Lee, K.<br/>
In *2014 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*<br/>
<span style="color:#E84A5F">**Best Paper Award**</span>

0. **Automatic detection of inferior alveolar nerve canal from cone-beam computed tomography images for dental surgery planning**<br/>
Choi, J.-H., **Baek, S.-Y.**, Kim, Y., Son, T.-G., Park, S., & Lee, K.<br/>
In *NEXTMED/MMVR21, Manhattan Beach, California, United States*

0. **Automatic algorithm for finding insertion axis of dental prosthesis**<br/>
Lim, J., **Baek, S.-Y.**, Lee, J., & Lee, K.<br/>
In *2014 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*<br/>

0. **An algorithm for estimating surface normal from its boundary curves**<br/>
Park, J.-S., Kim, T., **Baek, S.-Y.**, & Lee, K.<br/>
In *2014 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*<br/>
<span style="color:#E84A5F">**Best Student Paper Award**<br/>
{:start="30"}
{: reversed="reversed"}

<br/>&nbsp;

### 2013
0. **GaFinC: Gaze and finger control interface for 3D model manipulation in CAD application**<br/>
Song, J., Cho, S., **Baek, S.-Y.**, Lee, K., & Bang, H.<br/>
In *SIAM Conference on Geometric & Physical Modeling (GD/SPM13), Denver, Colorado, United States*<br/>
(<span style="color:#E84A5F">**Acceptance rate: 26.8%**</span>)
{:start="16"}
{: reversed="reversed"}

<br/>&nbsp;

### 2012
0. **Kinecad: A novel gesture-based CAD system using kinect**<br/>
Park, H., Lee, D., Yang, S., Lee, S., **Baek, S.-Y.**, & Lee, K.<br/>
In *2012 Asian Conference on Design and Digital Engineering (ACDDE2012), Hokkaido, Japan*

0. **Automated bone landmarks prediction on the femur using anatomical deformation technique**<br/>
**Baek, S.-Y.**, Wang, J. H., Song, I., Lee, K., & Koo, S.<br/>
In *Symposium on Solid and Physical Modeling (SPM2012), Dijon, France*<br/>
(<span style="color:#E84A5F">**Acceptance rate: 44%**</span>)

0. **Changes in medio-lateral knee joint reactions of flatfoot patients due to insole conditions**<br/>
Lee, S., **Baek, S.-Y.**, Son, J., Kim, D., & Lee, K.<br/>
In *18th Congress of the European Society of Biomechanics, Lisbon, Portugal*

0. **Statistical analysis of foot shape for designing mass-customized footwear**<br/>
**Baek, S.-Y.**, Son, J., & Lee, K.<br/>
In *9th International Symposium on Tools and Methods for Competitive Engineering (TMCE2012), Karsluhe, Germany*

0. **Automatic measurement of dimensions of 3D foot scan data**<br/>
Son, J., **Baek, S.-Y.**, & Lee, K.<br/>
In *Asian Workshop on 3D Body Scanning Technologies, Tokyo, Japan*

0. **Knowledge-based design framework for user-tailored insoles**<br/>
**Baek, S**, Son, J., & Lee, K.<br/>
In *Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*<br/>
<span style="color:#E84A5F">**Invited Talk**</span>

0. **Changes in medio-lateral knee joint reaction force of patients with over-pronation during gait due to insole parameters**<br/>
Lee, S., **Baek, S.-Y.**, Son, J., Kim, D., & Lee, K.<br/>
In *2012 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*

0. **An algorithm for automatic measurement of dimensions of 3D foot scan data**<br/>
Son, J., **Baek, S.-Y.**, & Lee, K.<br/>
In *2012 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*
{:start="15"}
{: reversed="reversed"}

<br/>&nbsp;

### 2011
0. **Deformation of raw 3D scan surfaces via multi-resolution RBF networks**<br/>
**Baek, S.-Y.**, Lee, J., & Lee, K.<br/>
In *Asian Workshop on 3D Body Scanning Technologies, Tokyo, Japan*

0. **Statistical deformation of femur geometry**<br/>
Jo, J., **Baek, S.-Y.**, Lee, K., Song, I.-s., & Koo, S.<br/>
In *2011 Spring Conference of the Korean Society of Mechanical Engineers, Pohang, Korea*

0. **3D generic vertebra model for computer aided diagnosis**<br/>
Lee, J., **Baek, S.-Y.**, & Lee, K.<br/>
In *2011 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*
{:start="7"}
{: reversed="reversed"}

<br/>&nbsp;

### 2010
0. **Parametric human body modeling system for virtual garment fitting**<br/>
**Baek, S.-Y.** & Lee, K.<br/>
In *8th International Symposium on Tools and Methods of Competitive Engineering (TMCE2010), Ancona, Italy.*

0. **Interactive parametric modeling of human body shape**<br/>
**Baek, S.-Y.** & Lee, K.<br/>
In *2010 Asian Conference on Design and Digital Engineering (ACDDE2010), Jeju, Korea*
{:start="4"}
{: reversed="reversed"}

<br/>&nbsp;

### 2009
0. **3D face model reconstruction from single 2D frontal image**<br/>
**Baek, S.-Y.**, Kim, B.-Y., & Lee, K.<br/>
In *8th ACM SIGGRAPH International Conference on Virtual Reality Continuum and Its Applications inIndustry (VRCAI ’09), Tokyo, Japan*<br/>
(<span style="color:#E84A5F">**Acceptance rate: 41%**</span>)

0. **Synthesis of human body shape for given body parameters us-ing3d body scan data**<br/>
Jang, T., **Baek, S.-Y.**, & Lee, K.<br/>
In *2009 Annual Conference of the Society of CAD/CAM Engineers, Pyeongchang, Korea*
{: reversed="reversed"}
 -->

