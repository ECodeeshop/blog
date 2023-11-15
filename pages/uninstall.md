---
title: Uninstall
permalink: "/uninstall/"
---

Redirecting...

<script>
try {

    const site_extensions = JSON.parse(`{{site.data.extensions}}`.replace(/=>/g, ':'))    
    const id = getQueryVariable("id");

    window.location.href = site_extensions[id][0].uninstall_form_url

    function getQueryVariable(variable) {
        var query = window.location.search.substring(1);
        var vars = query.split("&");
        for (var i=0;i<vars.length;i++) {
            var pair = vars[i].split("=");
            if (pair[0] == variable) {
            return pair[1];
            }
        } 
        
        console.log('Query Variable ' + variable + ' not found')
        // alert('Nothing to uninstall')
    }
} catch(err) {
    alert('Something went wrong')
}
</script>