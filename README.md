# Bob Buzzard's Lightning Design System Samples

Note: If the org you are installing into has a packaging namespace, you'll need to update the various lightning out applications to use the namespace, or you will get an empty page with an error in the JavaScript console.  For example, if the packaging namespace is bblightning the BBLeadBoardApp code needs to be changed to use this namespace from:

    $Lightning.use("c:BBSObjectBoardOutApp", function() {
            $Lightning.createComponent("c:BBSObjectBoard",
                                       {
								'SObjectType': 'Lead',
								'StageValueField' : 'Status',
								'FieldNames' : 'Company, FirstName, LastName, LeadSource',
								'ExcludeValues': 'Converted',
										},
                  "lightning",
                  function(cmp) {
                    // no further setup required - yet!
              });
        });

to:

    $Lightning.use("bblightning:BBSObjectBoardOutApp", function() {
            $Lightning.createComponent("bblightning:BBSObjectBoard",
                                       {
								'SObjectType': 'Lead',
								'StageValueField' : 'Status',
								'FieldNames' : 'Company, FirstName, LastName, LeadSource',
								'ExcludeValues': 'Converted',
										},
                  "lightning",
                  function(cmp) {
                    // no further setup required - yet!
              });

## Getting Started
Install the unmanaged package via the following link :

https://login.salesforce.com/packaging/installPackage.apexp?p0=04t24000000AqHA

(If you've installed an earlier version, you'll need to uninstall that before installing the latest, as unmanaged packages can't be upgraded.

## Sample 1 - Account and Contacts Edit
See the blog post at : http://bobbuzzard.blogspot.co.uk/2015/09/lightning-design-system-edit-parent-and.html

Access the page via a URL similar to the following - note that if you do not supply an accountId parameter you will receive an internal server error!

https://_domain_.lightning.force.com/bblightning/BBAccountContactEdit.app?accountId=_id_

e.g.

https://bblds-test-dev-ed.lightning.force.com/bblightning/BBAccountContactEdit.app?accountId=001o000000GXMt3

## Sample 2 - Responsive Design
See the blog post at : http://bobbuzzard.blogspot.co.uk/2015/10/responsive-design-with-lightning-design.html

Create a tab for the 'Blog Post' custom object and create a few blog posts. I usually add the images as attachments to the record and copy the ID from there. Your mileage may vary with other options.

Access the page via a URL similar to the following:

https://_domain_.lightning.force.com/bblightning/BBBlogHome.app

e.g.

https://bblds-test-dev-ed.lightning.force.com/bblightning/BBBlogHome.app

## Sample 3 - LDS Activity Timeline, Lightning Components and Visualforce
See the blog post at : http://bobbuzzard.blogspot.co.uk/2015/10/lds-activity-timeline-lightning.html

Access the page via a URL similar to the following:

https://_domain_._instance_.visual.force.com/apex/AccountOppTimeline?id=_accountId_

e.g.

https://bblds-dev-ed--c.eu5.visual.force.com/apex/AccountOppTimeline?id=00124000005U5ox

## Sample 4 - Board Anything with SLDS and Lightning Components

See the blog post at : http://bobbuzzard.blogspot.co.uk/2016/01/board-anything-with-slds-and-lightning.html

Access the Lead Board Visualforce page via a URL similar to the following:

https://_domain_._instance_.visual.force.com/apex/BBLeadBoard

e.g.

https://bblds-dev-ed--c.eu5.visual.force.com/apex/BBLeadBoard

Access the default case view app board via a URL similar to the following:

https://_domain_.lightning.force.com/c/BBSObjectBoardApp.app

e.g.

https://bblds-dev-ed.lightning.force.com/c/BBSObjectBoardApp.app

## Sample 5 - Lightning Design System in Visualforce Part 1 - Getting Started

See the blog post at : http://bobbuzzard.blogspot.co.uk/2016/12/lightning-design-system-in-visualforce.html

Access the page through a URL similar to the following : 

https://_domain_._instance_.visual.force.com/apex/BBLDS_VF_Record?id=_AccountId_

e.g.

https://bblds-dev-ed--c.eu5.visual.force.com/apex/BBLDS_VF_Form?id=00324000012S3jT

## Sample 6 - Lightning Design System in Visualforce Part 2 - Forms

See the blog post at : http://bobbuzzard.blogspot.co.uk/2017/02/lightning-design-system-in-visualforce.html

Access the page through a URL similar to the following : 

https://_domain_._instance_.visual.force.com/apex/BBLDS_VF_Form?id=_ContactId_

e.g.

https://bblds-dev-ed--c.eu5.visual.force.com/apex/BBLDS_VF_Form?id=00324000012S3jT
