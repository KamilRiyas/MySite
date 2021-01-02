<script>
    import { fade } from 'svelte/transition';
</script>

<div class="content" in:fade>
    <div class="project-holder">
        <div class="project-title">
            <div class="project-name"><h3>Talentbrew Apply</h3></div>
            <div class="project-duration"><p>July 2018 -  Till Date</p></div>
        </div>
        <div class="techs-involed">
            <div>.Net C#</div>
            <div>MVC/WebAPI</div>
            <div>Entity Framework</div>
            <div>node.js</div>
            <div>Web Scraping</div>
            <div>SQL Server</div>
        </div>
        <div class="project-description">
            <p class="description">Customization of prebuilt Application Talent Sites, so that the subscribed users can have better user experience compared to traditional job sites. The customizations involve scraping jobs from the client ATS, adding better UI, adding Google Analytics and Applicants tracking for user metrics.</p>
        </div>
    </div>
    <div class="project-holder">
        <div class="project-title">
            <div class="project-name"><h3>APS Automation</h3></div>
            <div class="project-duration"><p>May 2017 -  June 2018</p></div>
        </div>
        <div class="techs-involed">
            <div>.Net C#</div>
            <div>ADO.NET</div>
            <div>Powershell</div>
            <div>Web Forms</div>
            <div>SQL Server</div>
        </div>
        <div class="project-description">
            <p class="description">The goal of this project is to Automate the L3 support activities such as Server patching, decommissioning, Service Account password reset and stakeholders notifications for multiple business processes. It’s being enhanced on the existing Webforms application based on N-tier architecture backed by MS SQL Server.</p>
        </div>
    </div>
    <div class="project-holder">
        <div class="project-title">
            <div class="project-name"><h3>OutlierView3</h3></div>
            <div class="project-duration"><p>Feb 2016 -  Mar 2017</p></div>
        </div>
        <div class="techs-involed">
            <div>.Net C#</div>
            <div>MVC/WebAPI</div>
            <div>Entity Framework</div>
            <div>AngularJS</div>
            <div>System Design</div>
            <div>Business Analysis</div>
        </div>
        <div class="project-description">
            <p class="description">The goal of this project is to validate the claim level data from the federal states for all the Medicaid programs to find anomalies and highlight the rebate amounts that can be saved by drug manufacturers. The web application was implemented on MVC3 Framework and Angular JS with Web API.</p>
        </div>
    </div>
    <div class="project-holder">
        <div class="project-title">
            <div class="project-name"><h3>QC Report Automation</h3></div>
            <div class="project-duration"><p>Dec 2012 -  Jan 2017</p></div>
        </div>
        <div class="techs-involed">
            <div>.Net MVC</div>
            <div>Entity Framework</div>
            <div>SQL Server</div>
            <div>Excel VBA</div>
            <div>Highcharts</div>
        </div>
        <div class="project-description">
            <p class="description">The goal of this project is to automate the process of generating reports from HP Application Lifecycle Management. Based in the data presented in HP Quality Center, the project was implemented on MVC3 Framework with the OTA DLL library and REST service call, would populate the details and report. Data transactions were handled using Entity Framework. </p>
        </div>
    </div>
    <div class="project-holder">
        <div class="project-title">
            <div class="project-name"><h3>MyEYOnline / One Global System</h3></div>
            <div class="project-duration"><p>Jan 2011 -  Dec 2012</p></div>
        </div>
        <div class="techs-involed">
            <div>.Net MVC</div>
            <div>Entity Framework</div>
            <div>SQL Server</div>
            <div>Razor</div>
        </div>
        <div class="project-description">
            <p class="description">The goal of this project is to redesign the previously existing Client Portal over MVC3 framework. The target of the redesign process was to provide faster client side rendering and minimize the overheads that existed in the previous application.</p>
        </div>
    </div>
</div>

<style>
    .content{
        display: flex;
        flex-direction: column;
    }
    .project-title{
        display: flex;
        flex-direction: row;
    }
    .project-duration{
        padding-top:4px;
    }
    .project-title>div{
        margin:5px;
    }
    .techs-involed{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
    }
    .techs-involed>div{
        background-color: antiquewhite;
        margin: 5px;
        padding: 5px;
    }
    .description{
        text-align: start;
    }

    @media only screen and (max-width: 600px) {
        .content{
            width: 350px;
        }
        .techs-involed{
            flex-wrap: wrap;
        }
    }
</style>