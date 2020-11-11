## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:de5b23a8826e65de497ac7335464d39371cbda3c5c4a3c0b3a3c2a816ad67149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull caddy@sha256:405a17b713c3f1517124a2506ac9b4ed33285819013417e6b90fb2aa07cb0bd6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5802615067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371225d0afbf64a113a3745e99535e2e17239829f4e36d99aa36e7aee3be9efc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 20:56:04 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 11 Nov 2020 20:56:05 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 11 Nov 2020 20:57:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 11 Nov 2020 20:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 11 Nov 2020 20:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 11 Nov 2020 20:57:28 GMT
VOLUME [c:/config]
# Wed, 11 Nov 2020 20:57:29 GMT
VOLUME [c:/data]
# Wed, 11 Nov 2020 20:57:30 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 11 Nov 2020 20:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Nov 2020 20:57:31 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Nov 2020 20:57:32 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Nov 2020 20:57:32 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Nov 2020 20:57:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Nov 2020 20:57:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Nov 2020 20:57:35 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Nov 2020 20:57:35 GMT
EXPOSE 80
# Wed, 11 Nov 2020 20:57:36 GMT
EXPOSE 443
# Wed, 11 Nov 2020 20:57:37 GMT
EXPOSE 2019
# Wed, 11 Nov 2020 20:58:18 GMT
RUN caddy version
# Wed, 11 Nov 2020 20:58:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5595cf12db880fdffb7bc7e0ceef81a68e0766ff34fdc357635566a05b60085`  
		Last Modified: Wed, 11 Nov 2020 21:03:35 GMT  
		Size: 10.1 MB (10089893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47fc9d917c611e97ffa642af414764e4712d012a3b2c10700a357a771d58bf3`  
		Last Modified: Wed, 11 Nov 2020 21:03:24 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2b332d20177fb217e2744454885bba6eb94e9c7512c35bef53cf1222f10b3a`  
		Last Modified: Wed, 11 Nov 2020 21:03:50 GMT  
		Size: 21.7 MB (21694741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061740784584c807be44f52e632b6fcafa7893cab07ca93723103ca41e759cd2`  
		Last Modified: Wed, 11 Nov 2020 21:03:23 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a051df7f978fd750beb5e55b7a7da2d50550a52c97baf897cd3452347196147`  
		Last Modified: Wed, 11 Nov 2020 21:03:23 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94db8d6fb716d4c43b34e09a05176f94701accb480ce613c231d70ef23c649b`  
		Last Modified: Wed, 11 Nov 2020 21:03:20 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eeb5cfdcdca36082954b3510135aea31966da19679b9cc7d8d4e43a3892f2f5`  
		Last Modified: Wed, 11 Nov 2020 21:03:19 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc11877f41dad7cb21c9e61379268e564a03b044ec4cfb124cccd267ef551c`  
		Last Modified: Wed, 11 Nov 2020 21:03:21 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9914893b848ce6d71a6f99575e794219e1603afe1dcee2bcbf69f3a41451ab05`  
		Last Modified: Wed, 11 Nov 2020 21:03:20 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab52b473d299810d7e49b3d9d98db42e6aa57e5426b79f4cd7f68fd766a8a9b`  
		Last Modified: Wed, 11 Nov 2020 21:03:20 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3333f590132f229c9979af102fd15c4a5958d9e3d94d50632eeb045c14028ac1`  
		Last Modified: Wed, 11 Nov 2020 21:03:17 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c4e6df6d5faa8f29b56e44eb52dc65c9d6795322a0e6d743a9d373f97adf9`  
		Last Modified: Wed, 11 Nov 2020 21:03:17 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a015ed900b4c4b4d23631449b68473b1e31eda520fa22c7c19a845ac6f133f31`  
		Last Modified: Wed, 11 Nov 2020 21:03:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f354d2a4fb61ae55364b2ae298552e22165583c076c39e05707e906633b8a2`  
		Last Modified: Wed, 11 Nov 2020 21:03:17 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc11e1af39f958f492359f3242aa5205230791b166e14ab2f94067e9999464e`  
		Last Modified: Wed, 11 Nov 2020 21:03:16 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680a4e622ed285e795cc2fd731f38022c2e6ca478f2223fb9fcafe0a61b5e969`  
		Last Modified: Wed, 11 Nov 2020 21:03:13 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f936683e767d2733a4a898519ce7c8bc6a608fede4e7cc04c41b5fed180287`  
		Last Modified: Wed, 11 Nov 2020 21:03:13 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4fbe6665c83c229d90ec42acce959b356dbf1a97ca281604625a29d8437133`  
		Last Modified: Wed, 11 Nov 2020 21:03:13 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6966c1a2733b248361e0fbafefb3b58805b223ef954ced160cb1ca7f239c25`  
		Last Modified: Wed, 11 Nov 2020 21:03:13 GMT  
		Size: 251.9 KB (251913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3d08972458dc80b8c379340207e2cfeee9ea33d9e9e405ebbf52421ef16dd5`  
		Last Modified: Wed, 11 Nov 2020 21:03:13 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
