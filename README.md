# HotspotRF Zoho CRM Integration

You can now easily integrate HotspotRF's API into Zoho CRM. This is perfect for those looking to filter through their leads - fast and efficiently. Let's say a potential user is interested in becoming a host. They go to your website, apply to become a host and that information is sent to Zoho CRM. Well now you have to figure out the earnings for that location by manually inputting the information you've gathered from your website's form into https://app.hotspotrf.com/map. Now with the click of a button, you can populate that information directly into your CRM! Continue reading on how to get that setup.

# How?

Great question! In this tutorial it is expected to have an alright understanding of Zoho CRM. Understand that this is a two part guide: You will need to complete part one, in order to move onto part two. Your website will also need to input information from the form of your website to Zoho CRM.

## Part One

1) Enter the "Setup Page" of your Zoho CRM by clicking the "gear" icon at the top right hand corner.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/1.png">
</p>
2) Type "Layout" in the search bar and select "Layouts".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/1_.png">
</p>
3) In your "Layouts" select "Standard".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/2_.png">
</p>
4) You will need to make a new section called "HotspotRF" and for it look like that of the screenshot below.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/3_.png">
</p>
5) Be sure to have another section called "Host Address Info" and for it to look like the screenshot below.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/4_.png">
</p> 
6) You'll also want to make sure the "Terrain" field has the options the same as the screenshot below.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/5_.png">
</p> 

The "Host Address Info" comes from your website once a lead comes in and is required for this to function; especially "Terrain", "Floor Level", and "Full Address".

## Part Two

1) First you'll want to be logged into your Zoho CRM: https://crm.zoho.com/
2) Navigate to Zoho CRM Setup Page by clicking the "gear" icon at the top right hand corner.
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/1.png">
</p>
3) Get to your Functions page by selectiong 'functions' under 'developer space' in Zoho CRM Setup Page.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/2.png">
</p>
4) In your "My Functions" tab, click the button "New Function".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/3.png">
</p>
5) A new window will pop-up called "Create New Function". Put "Lead_enrichment_with_Hotspot_RF_Button" as both the "Function Name" and "Display Name", the description as "Enrich a lead with HotspotRF API." and "Category" as "Button". Once completed, you'll want to click the blue button "Create".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/4.png">
</p>
6) Put all the contents of the https://github.com/hotspotrf/zoho/blob/main/Lead_Enrichment_with_Hotspot_RF_Button into the editor. <b>Be sure to update the API key vairable with your API at line 26 or else it will not work.</b> Now click the "Edit Arguments" link.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/5.png">
</p>
7) Once the "Edit Arguments" pop-up appears, under "Function Arguments", you'll want to put "LeadID" and mark it as a "string"; click save.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/6.png">
</p>
8) That's it, now save your function by clicking the blue button "Save".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/7.png">
</p>
9) You'll need to once again navigate to Zoho CRM Setup Page by clicking the 'gear' icon at the top right hand corner.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/8.png">
</p>
10) In the search box you'll want to type in "button" and select the first result "Links and Buttons".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/9.png">
</p>
11) You now should be under "Modules" -> "Leads" -> "Links and Buttons". Now click "New Button" next to "New Link".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/10.png">
</p>
12) Under "Create Your Button" you'll want to enter "HotspotRF Enrichment" under "What would you like to name the button?" and the description as "Click me to enrich a lead."<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/11.png">
</p>
13) You'll now need a place to put your button. Under "Where would you like to place the button?", select "View Page".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/12.png">
</p>
14) We have the button made, function ready, now to point that button to our function by selecting "From Existing Actions" under "What action would you like the button to preform?"<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/13.png">
</p>
15) When the window "Existing Actions" appears, click the "Configure" next to the "Lead_Enrichment_with_Hotspot_RF_Button".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/14.png">
</p>
16) Scroll down a little under the "Configure Function" window and type in "#" - that's it - as the value for "LeadID". You'll now see a little pop-up to which you'll select "Lead Id" and click "Done".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/15.png">
</p>
17) After completion of "Configure Function", you'll want to click the blue button "Save".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/16.png">
</p>
18) Now you save your newly created button by clicking "Save".<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/17.png">
</p>
19) At this point the function has been made, button made and linked to your button, you can now load up a lead - as you usually would - to see a new button next to "Edit" that says "HotspotRF Enrichment". Feel free to click that.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/18.png">
</p>
20) Once the button is clicked, the function is fired and a simulation is ran. Upon a successful simulation, you'll get a message.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/19.png">
</p>
21) Upon exiting the pop-up, the page is refreshed and the HNT rewards are filled in.<br/><br/>
<p align="center">
  <img src="https://hotspotrf.com/imgs/github/20.png">
</p>

If you have any questions about this or comments and concerns, feel free to message us directly at hello@hotspotrf.com.
