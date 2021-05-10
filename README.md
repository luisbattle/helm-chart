# helm-chart

## create repo chart(github)
I’d like to avoid bot crawling on my repository, so I add the following robots.txt file:
<pre>
echo -e “User-Agent: *\nDisallow: /” > robots.txt
</pre>

## Lint the chart
helm lint runs a series of tests to verify that
the chart is well-formed
<pre>
helm lint chart/
==> Linting chart/

1 chart(s) linted, 0 chart(s) failed
</pre>

# Create chart Package
<pre>
helm package chart/
Successfully packaged chart and saved it to: /repositories/helm-chart/node-application-server-1.0.0.tgz
</pre>


## add helm repo from github
<pre>
helm repo add myhelmrepo 'https://raw.github.com/kmzfs/helm-repo-in-github/master'
"myhelmrepo" has been added to your repositories
</pre>