---
layout: breadcrumbs
permalink: "/workshop"
title: "Mom's Workshop: Build Your Custom Bot!"
name: "Mom's Workshop: Build Your Custom Bot!"
description: "Use this Custom Bot Builder to showcase and share all your great ideas!"
breadcrumbs:
  Community Adventure: "/#community"
---

<style type="text/css">
    .botcard {
        border-radius: 10px;
        width: 240px;
        display: flex;
        flex-direction: column;
        margin: 0 auto;
    }
    .actual-card{
      margin-bottom: 20px;
    }
    .pic {
    background: linear-gradient(160deg, #1b1a6b 50%, cyan);
}
    .cardinfos {
        background: #246eff;
    }
    .cardinfos * {
        font-weight: 1000;
    }
    
    .cardinfos table {
        overflow-x: hidden;
        margin: 0px;
    }
    .bot_bloc_4{
      width: 100%;
    }
        #clipboard {
            background-color: transparent;
            color: transparent;
            border: none;
            padding: none;
            }
        .barbackground {
            background-color: beige;
            padding: 0px;
            margin: 2px 0px 3px 0px;
            height: 20px;
            max-width: 320px;
            border-radius: 10px;
        }
        #dps-bar, #health-bar, #speed-bar, #attack-bar {
            padding: 0px;
            margin: 0px;
            height: 20px;
            background-image: linear-gradient(to right, blue, rgb(50, 50, 95));
            border-radius: 10px;
        }
        #dps-bar > p , #health-bar > p, #speed-bar > p, #attack-bar > p {
            color: rgb(174, 240, 200);
            font-weight: bold;
            margin: 0px;
            padding: 1px 0px 0px 10px;
        }
  button {
    text-decoration: none;
    font-weight: bold;
    color: white;
    display: inline-block;
    padding: 5px;
    width: fit-content;
    border-radius: 15px 5px;
    text-shadow: 2px 2px 3px rgb(0 0 0 / 46%);
    box-shadow: 3px 3px 5px rgb(0 0 0 / 48%);
    border: 2px solid rgba(255, 255, 255, 0.388);
    margin: 10px 5px;
    background-image: linear-gradient(45deg, rgb(4, 50, 100), rgb(0, 119, 128));
}
</style>

<h3>Mom's Workshop: Build Your Custom Bot!</h3>
<div>
  <ul>
    <li><strong>Create your Bot</strong>: click any text, image, or stats bar, to edit it.</li>
    <li>
        <strong>Share the link</strong>: <button onclick="copyClipboard()">Copy URL</button>, then use an <a href="https://tinyurl.com/">url shortener</a>
        <input id="clipboard" type="text" readonly="">
    </li>
    <li><strong>Share as a picture</strong>: <a id="exporttoimage" href="/workshop-export">click here to export as a compact picture</a></li>
    <li>
      <strong>Save in your browser</strong>: <button onclick="localSave()">Save</button> (supported browsers only)
      <ul id="savedBotsList"></ul>
    </li>
  </ul>
</div>

<div class="bot-infos">
    <div class="bot_bloc_1">
        <div class="intro">
            <h1 class="custom-edit custom-edit-name">Custom Bot name...</h1>

            <p><code class="custom-edit custom-edit-desc">Custom Bot description...</code></p>
        </div>
        <div class="botcard">
          <div class="actual-card">
            <div class="pic">
                <p><img loading="lazy" src="/assets/img/icons/cog.png" class="custom-edit custom-edit-image" /></p>
            </div>
            <div class="cardinfos">
                <table>
                  <thead>
                    <tr>
                      <th>Type</th>
                      <th>Rarity</th>
                      <th>Acquisition</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td class="custom-edit custom-edit-class">Class...</td>
                      <td class="custom-edit custom-edit-rarity">Rarity...</td>
                      <td class="custom-edit custom-edit-acquisition">Acquisition...</td>
                    </tr>
                  </tbody>
                </table>
            </div>
          </div>
          <div>
            <h3 id="overview">Overview</h3>
            <div>
              <p class="custom-edit custom-edit-overview">Overview of your bot...</p>
              <p><a href="#comments" title="Comments, AI Builds, tips & tricks...">AI Builds, Tips, etc.</a></p>
            </div>

          </div>
        </div>

        <div class="abilities">
            <h2 id="abilities">Abilities</h2>

            <ul>
              <li>
                <p><h3 class="custom-edit custom-edit-ability1name">1st Ability Name...</h3><code class="custom-edit custom-edit-ability1infos">infos...</code></p>
                <p class="custom-edit custom-edit-ability1desc">description...</p>
              </li>
              <li>
                <p><h3 class="custom-edit custom-edit-ability2name">2st Ability Name...</h3><code class="custom-edit custom-edit-ability2infos">infos...</code></p>
                <p class="custom-edit custom-edit-ability2desc">description...</p>
              </li>
              <li>
                <p><h3 class="custom-edit custom-edit-ability3name">3st Ability Name...</h3><code class="custom-edit custom-edit-ability3infos">infos...</code></p>
                <p class="custom-edit custom-edit-ability3desc">description...</p>
              </li>
            </ul>
        </div>
    </div>

    <div class="bot_bloc_2">

        <h2 id="ai-tree">AI tree</h2>

        <ul>
          <li>
            <p>AI Level 1 (500xp)</p>

            <table>
              <thead>
                <tr>
                  <th class="custom-edit custom-edit-ai1aName">ai1aName...</th>
                  <th class="custom-edit custom-edit-ai1bName">ai1bName...</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td class="custom-edit custom-edit-ai1aDesc">ai1aDescription...</td>
                  <td class="custom-edit custom-edit-ai1bDesc">ai1bDescription...</td>
                </tr>
              </tbody>
            </table>
          </li>
          <li>
            <p>AI Level 2 (2000xp)</p>

            <table>
              <thead>
                <tr>
                  <th class="custom-edit custom-edit-ai2aName">ai2aName...</th>
                  <th class="custom-edit custom-edit-ai2bName">ai2bName...</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td class="custom-edit custom-edit-ai2aDesc">ai2aDescription...</td>
                  <td class="custom-edit custom-edit-ai2bDesc">ai2bDescription...</td>
                </tr>
              </tbody>
            </table>
          </li>
          <li>
            <p>AI Level 3 (5000xp)</p>

            <table>
              <thead>
                <tr>
                  <th class="custom-edit custom-edit-ai3aName">ai3aName...</th>
                  <th class="custom-edit custom-edit-ai3bName">ai3bName...</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td class="custom-edit custom-edit-ai3aDesc">ai3aDescription...</td>
                  <td class="custom-edit custom-edit-ai3bDesc">ai3bDescription...</td>
                </tr>
              </tbody>
            </table>
          </li>
          <li>
            <p>AI Level 4 (14000xp)</p>

            <table>
              <thead>
                <tr>
                  <th class="custom-edit custom-edit-ai4aName">ai4aName...</th>
                  <th class="custom-edit custom-edit-ai4bName">ai4bName...</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td class="custom-edit custom-edit-ai4aDesc">ai4aDescription...</td>
                  <td class="custom-edit custom-edit-ai4bDesc">ai4bDescription...</td>
                </tr>
              </tbody>
            </table>
          </li>
          <li>
            <p>AI Level 5 (30000xp)</p>

            <table>
              <thead>
                <tr>
                  <th class="custom-edit custom-edit-ai5aName">ai5aName...</th>
                  <th class="custom-edit custom-edit-ai5bName">ai5bName...</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td class="custom-edit custom-edit-ai5aDesc">ai5aDescription...</td>
                  <td class="custom-edit custom-edit-ai5bDesc">ai5bDescription...</td>
                </tr>
              </tbody>
            </table>
          </li>
        </ul>
    </div>
    <div class="bot_bloc_3">
        <div class="stats">
            
            <h2 id="stats">Stats</h2>
            
    <div class="barbackground"><div id="attack-bar"><p>Attack</p></div></div>
    <div class="barbackground"><div id="health-bar"><p>Health</p></div></div>   
    <div class="barbackground"><div id="dps-bar"><p>DPS</p></div></div> 
    <div class="barbackground"><div id="speed-bar"><p>Speed</p></div></div>

        </div>

      <div class="bot_bloc_3">
        <h2 id="concept-art">Concept Art</h2>
        <img loading="lazy" src="/assets/img/icons/cog.png" class="custom-edit custom-edit-conceptArt" />
      </div>

      <div class="bot_bloc_4">
        <h2 id="comments">Comments</h2>
          <p class="custom-edit custom-edit-notes">Notes...</p>
        <h3 id="creators">Creators</h3>
          <p class="custom-edit custom-edit-creators">Notes...</p>
        <p>Last updated at: <span class="custom-edit custom-edit-updatedAt"></span></p>
      </div>
</div>


<script type="text/javascript">

    // global state with all the updated values. Serialized/b64 encoded into the anchor.
    var gState = {
        'updatedAt': "",
        'name': "Bot Name...",
        'desc': "Click to edit the description..."
    };

    // Do we have an anchor already?
    var anchor = document.location.hash;
    if (anchor){
        // If yes, get the app state out of it
        gState = extractFromAnchor(anchor);
        console.log(gState);
  
    //Export to Image Link Builder
      document.querySelector('#exporttoimage').href = 'https://www.botworld.wiki/workshop-export' + anchor
  
    }
    // then initialize the app with it
    initFromState(gState);
    initButtonsInputs();

    function initButtonsInputs(){
        document.querySelectorAll('.custom-edit').forEach(($el) => $el.onclick = clickToEdit);
        document.querySelector('.custom-edit-image').onclick = editImageUrl;
        document.querySelector('.custom-edit-conceptArt').onclick = editConceptUrl;
    }

    function editImageUrl(){
        var $img = document.querySelector('.custom-edit-image'); 
        var response = prompt("Edit the image URL", $img.src);
        response = (response === null)? $img.src : response;
        $img.src = response;
        updateState('image', response);
    }
    function editConceptUrl(){
        var $img = document.querySelector('.custom-edit-conceptArt'); 
        var response = prompt("Edit the concept art image URL", $img.src);
        response = (response === null)? $img.src : response;
        $img.src = response;
        updateState('conceptArt', response);
    }
    function clickToEdit(e){
        var $el = e.target;
        var editedFieldId = getCustomEditId($el);
        var response = prompt("Edit the field: "+editedFieldId, $el.innerText);
        response = (response === null)? $el.innerText : response;
  response = (response.match(/^\s*$/)?.length)? "-" : response;
        var newFieldValue = response;
        $el.innerText = newFieldValue;
        updateState(editedFieldId, newFieldValue);
    }
    function updateState(id, val){
        gState[id] = val;
        gState['updatedAt'] = new Date().toString();
        document.querySelector('.custom-edit-updatedAt').innerText = gState['updatedAt'];
        exportState();
        anchor = document.location.hash;
        document.querySelector('#exporttoimage').href = 'https://www.botworld.wiki/workshop-export' + anchor;
    }

    function getCustomEditId($el){
        return Array.from($el.classList).filter((className) => className.startsWith('custom-edit-'))[0].slice('custom-edit-'.length)
    }


    function exportState(){
        // we do the reverse than in extractFromAnchor()
        var data = JSON.stringify(gState);
        var encoded = btoa(data);
        var anchor = '#'+encoded;
        // update the anchor
        document.location.hash = anchor;
    }


    function extractFromAnchor(anchor){
        // remove the #
        var data = anchor.slice(1);
        // the data will be base64-encoded to avoid special characters issues
        var decoded = atob(data) 
        // let's assume we serialize the data as json
        return JSON.parse(decoded);
    }


    // paste all the values from the url into the page
    function initFromState(state){
        document.querySelectorAll('.custom-edit').forEach( ($el) => {
            var fieldId = getCustomEditId($el);
            if (fieldId in gState){
                $el.innerText = gState[fieldId];
            }
        })
        if ('image' in gState) document.querySelector('.custom-edit-image').src = gState['image'];
        if ('conceptArt' in gState) document.querySelector('.custom-edit-conceptArt').src = gState['conceptArt'];
        if ('attackBar' in gState) {document.querySelector('#attack-bar').style.width = gState['attackBar']};
        if ('dpsBar' in gState) {document.querySelector('#dps-bar').style.width = gState['dpsBar']};
        if ('healthBar' in gState) {document.querySelector('#health-bar').style.width = gState['healthBar']};
        if ('speedBar' in gState) {document.querySelector('#speed-bar').style.width = gState['speedBar']};
    }
  function copyClipboard(text) {
        document.getElementById("clipboard").value = window.location.href
        clipboard.focus()
        clipboard.select()
        document.execCommand('copy')
        alert("Copied!")
        }

        function clickInputs(){
            document.querySelector('#attack-bar p').onclick = attackProgress;
            document.querySelector('#health-bar p').onclick = healthProgress;
            document.querySelector('#dps-bar p').onclick = dpsProgress;
            document.querySelector('#speed-bar p').onclick = speedProgress
        }
        clickInputs();

        function attackProgress(text) {
            var attackInput = window.prompt('Type your bot attack in a 1 to 100 range')
            if (attackInput >= 0 && attackInput <= 100) {
            attackInput = attackInput
            } else {
            attackInput = 100
            window.alert('Error: input must be a number between 0 and 100')
            }
            var $attackBar = document.querySelector('#attack-bar')
            var attackValue = attackInput + '%'
            $attackBar.style.width = attackValue
            gState.attackBar = attackValue
            exportState()
        }

        function dpsProgress(text) {
            var dpsInput = window.prompt('Type your bot dps in a 1 to 100 range');
            if (dpsInput >= 0 && dpsInput <= 100) {
            dpsInput = dpsInput
            } else {
            dpsInput = 100
            window.alert('Error: input must be a number between 0 and 100')
            }
            var $dpsBar = document.querySelector('#dps-bar');
            var dpsValue = dpsInput + '%'
            $dpsBar.style.width = dpsValue
            gState.dpsBar = dpsValue
            exportState()
        }

        function healthProgress(text) {
            var healthInput = window.prompt('Type your bot health in a 1 to 100 range');
            if (healthInput >= 0 && healthInput <= 100) {
            healthInput = healthInput 
            } else {
            healthInput = 100
            window.alert('Error: input must be a number between 0 and 100')
            }
            var $healthBar = document.querySelector('#health-bar');
            var healthValue = healthInput + '%'
            $healthBar.style.width = healthValue
            gState.healthBar = healthValue
            exportState()
        }

        function speedProgress(text){
            var speedInput = window.prompt('Type your bot speed in a 1 to 100 range');
            if (speedInput >= 0 && speedInput <= 100) {
            speedInput = speedInput 
            } else {
            speedInput = 100
            window.alert('Error: input must be a number between 0 and 100')
            }
            var $speedBar = document.querySelector('#speed-bar');
            var speedValue = speedInput + '%'
            $speedBar.style.width = speedValue
            gState.speedBar = speedValue
            exportState()
        }
</script>


<script type="text/javascript">

    /* Saving custom bots drafts in localStorage */
    
    localStorage['customBots'] = localStorage['customBots'] || '{}';
    var locallySavedBots = JSON.parse(localStorage['customBots']);

    function localSave(){
        if (!(gState.name in locallySavedBots)){ locallySavedBots[gState.name] = {} }
        Object.assign(locallySavedBots[gState.name], gState);
        localStorage['customBots'] = JSON.stringify(locallySavedBots);
        displaySavedBots();
    }
    function displaySavedBots(){
        const $ul = document.querySelector('#savedBotsList');
        //clear
        $ul.innerHTML = '';
        // create a <li> for each bot in localStorage
        for (var botname in locallySavedBots){
            let $li = document.createElement('li');
            $li.innerText = botname;
            // add a Load button to each
            let $load = document.createElement('button');
            $load.innerText = "Load";
            $load.setAttribute('target', botname);
            $load.onclick = loadSavedBot;
            $li.appendChild($load);
            // add a Delete button to each
            let $delete = document.createElement('button');
            $delete.innerText = "Delete";
            $delete.setAttribute('target', botname);
            $delete.onclick = deleteSavedBot;
            $li.appendChild($delete);
            // add the li+buttons to the list
            $ul.appendChild($li);

        }
    }
    displaySavedBots();

    function loadSavedBot(event){
        var targetSavedBot = event.target.getAttribute('target');
        gState = locallySavedBots[targetSavedBot];
        initFromState();
        exportState();
    }
    function deleteSavedBot(event){
        console.log
        var targetSavedBot = event.target.getAttribute('target');
        console.log('delete '+targetSavedBot)
        delete locallySavedBots[targetSavedBot];
        localStorage['customBots'] = JSON.stringify(locallySavedBots);
        displaySavedBots();
    }
</script>
  
