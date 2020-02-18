# Vitess@k8s

1. You need install vitess into default namespace ( the same namespace with etcd-opertator installed)

2. vtctld's web port with /app2 404 issue

   Solution: 
    Modify https://github.com/vitessio/vitess/blob/f3e541965bb498aea2d4015785f3c0db12bc2439/helm/vitess/templates/_vtctld.tpl
    
    Make sure 
                -web_dir="/vt/web/vtctld"
                -web_dir2="/vt/web/vtctld2/app"
    is added.
    
