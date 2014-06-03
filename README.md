# Base cartridge for Red Hat Presentations

This is base cartridge for creating Red Hat presentation using Reveal.js.

To use this cartridge register on www.openshift.com or use OpenShift Enterprise/Origin then follow the below steps.


1. Create a new gear using the metadata/manifest.yml file in this repo like this:

		rhc app create -n <namespace> -a <appname> <url to manifest.yml>
		
		for example:
		rhc app create -n pres0 -a web https://github.com/tqvarnst/webpreso-cartridge/raw/master/metadata/manifest.yml
		
	
		
2. Clone to your desktop (see openshift documentation)

* Update index.html or another html file with your presentation. *For more tips and tricks see the example.html file* 

* Commit and push to your gear
	
		git commit -a -m "Commit comment" && git push origin
		
* Go to your openshift URL (in the example above the link becomes [http://web-pres0.rhcloud.com](http://web-pres0.rhcloud.com)) to the see the presentation. 

* To print the presentation to a pdf add ?print-pdf (e.g. [http://web-pres0.rhcloud.com?print-pdf](http://web-pres0.rhcloud.com?print-pdf)) to the url in Google Chrome and use the print function in Chrome.
