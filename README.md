docker run -d --hostname gitlab.vyakhir.com \
-p 80:80 -p 22:22 -p 443:443 \
--name gitlab \
--restart always \
-e GITLAB_SKIP_UNMIGRATED_DATA_CHECK=true \
-v /home/gitlab/config:/etc/gitlab \
-v /home/gitlab/logs:/var/log/gitlab \
-v /home/gitlab/data:/var/opt/gitlab \
-v /home/gitlab/backups:/backups \
gitlab/gitlab-ce:16.7.2-ce.0
