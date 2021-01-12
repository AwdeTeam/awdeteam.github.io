---
title: Create a Procedure
layout: procedure
---

{% capture description %}
This is the procedure for... creating a new procedure! This standardizes the procedures so that we
can work off a shared format.
{% endcapture %}

{% capture steps %}
If you don't have the site repository, clone it with `$ git clone AwdeTeam/awdeteam.github.io`
Otherwise, just update it with `$ git pull`
Copy this file (`procedures/create-procedure.md`) with a descriptive (`kebab-case`) name for your new procedure.
Replace the `description` and `steps` with relevant content. (`steps` is newline-separated, so each newline gets a new step in the list)
Add a link to the new procedure in the `procedures.md` document under `# Procedure List`
{% endcapture %}

{% include templates/procedure.md name=page.title description=description steps=steps %}
