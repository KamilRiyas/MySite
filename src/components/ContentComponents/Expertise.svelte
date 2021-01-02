<script>
    import { fade } from 'svelte/transition';
    import MediaQuery from "svelte-media-query";
</script>

<MediaQuery query="(min-width: 501px) " let:matches>
    {#if matches}
    <div in:fade class="content">
        <p>I'm a full-stack developer with focus on Web Applications primarily on dotnet, now exploring JAMStack. I have over 10 years of Experience in all phases of SDLC. Apart from my work I like to explore and play around with all the latest tools and technologies. </p>
        <p>Below is my skillset</p>
        <div class="normal-skills-holder">
            <div class="normal-skills-category">
                FondEnd
            </div>
            <div class="skills">
                <div>HTML</div>
                <div>CSS</div>
                <div>Javascript/jQuery</div>
                <div>Svelte</div>
                <div>AngularJS</div>
            </div>
        </div>
        <div class="normal-skills-holder">
            <div class="normal-skills-category">
                Backend
            </div>
            <div class="skills">
                <div>.Net C#</div>
                <div>WebAPI/MVC</div>
                <div>node.js/jQuery</div>
            </div>
        </div>
        <div class="normal-skills-holder">
            <div class="normal-skills-category">
                Databases
            </div>
            <div class="skills">
                <div>SQL Server</div>
                <div>Postgres</div>
                <div>MongoDB</div>
            </div>
        </div>
        <div class="normal-skills-holder">
            <div class="normal-skills-category">
                Others
            </div>
            <div class="skills">
                <div>Cloud Solutions</div>
                <div>System Design</div>
                <div>Machine Learning</div>
            </div>
        </div>
        <p><strong>Fun fact: </strong>This site is built using just Svelte & HTML/CSS</p>
    </div>
    {/if}
</MediaQuery>

<MediaQuery query="(max-width: 500px)" let:matches>
    {#if matches}
    <div in:fade class="content mobile">
        <p>I'm a full-stack developer with focus on Web Applications primarily on dotnet, now exploring JAMStack. I have over 10 years of Experience in all phases of SDLC. Apart from my work I like to explore and play around with all the latest tools and technologies. </p>
        <div class="skills-holder">
            <div class="skills-category">
                FondEnd
            </div>
            <div class="skills">
                <div>HTML</div>
                <div>CSS</div>
                <div>Javascript/jQuery</div>
                <div>Svelte</div>
                <div>Bootstrap</div>
            </div>
        </div>
        <div class="skills-holder">
            <div class="skills-category">
                Backend
            </div>
            <div class="skills">
                <div>.Net C#</div>
                <div>WebAPI/MVC</div>
                <div>node.js/jQuery</div>
            </div>
        </div>
        <div class="skills-holder">
            <div class="skills-category">
                Databases
            </div>
            <div class="skills">
                <div>SQL Server</div>
                <div>Postgres</div>
                <div>MongoDB</div>
            </div>
        </div>
        <div class="skills-holder">
            <div class="skills-category">
                Others
            </div>
            <div class="skills">
                <div>Azure</div>
                <div>Powershell</div>
                <div>Machine Learning</div>
            </div>
        </div>
        <p><strong>Fun fact: </strong>This site was built using Svelte & HTML/CSS</p>
    </div>
    {/if}
</MediaQuery>

<style>
    .mobile{
        width: 350px;
    }
    .skills-category{
        font-weight: bold;
    }
    .skills{
        display: flex;
        justify-content: center;
    }
    .skills > div{
        background-color: antiquewhite;
        margin: 5px;
        padding: 5px;
    }

    .normal-skills-holder{
        display: flex;
        flex-direction: row;
        justify-content: start;
    }

    .normal-skills-category{
        font-weight: bold;
        width: 75px;
        margin:5px 5px 5px 25px;
        padding: 5px;
        text-align: start;
    }
</style>