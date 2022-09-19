## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:2c97b4a3cdc6d557346820a94041db5986de346e3a5fc61ab34aa775b3b9023d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:8d624ea27335666ac13a0fd06dab4a26ce6ef043121f2abefcd717398c247055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.0 MB (611011488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6efb92c7dbbb8171cec25faae0f51a4dbdfca952d117c717a1f0db33fa8cd9c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:04:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:04:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 02 Sep 2022 03:04:30 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Mon, 19 Sep 2022 17:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 19 Sep 2022 17:58:12 GMT
EXPOSE 11345
# Mon, 19 Sep 2022 17:58:12 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 19 Sep 2022 17:58:12 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 19 Sep 2022 17:58:12 GMT
CMD ["gzserver"]
# Mon, 19 Sep 2022 18:03:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8ce8f12b936a84cd04066c6c8c2863810f84eb09278e546e042e0841169145`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 16.2 MB (16177585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aef008ab8a7eed7c87b3dc23a1d4fcdcfc73ccb46684489914a3b3df0a77f5`  
		Last Modified: Fri, 02 Sep 2022 03:15:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabbcf7f742c339cfd6b82615934e775c27e221f6f005d86d2a83242189ab370`  
		Last Modified: Fri, 02 Sep 2022 03:15:35 GMT  
		Size: 5.5 KB (5497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1537bcb508d2f50cd79b45c314061a703adc222baed502921220df85ab0c0c9`  
		Last Modified: Mon, 19 Sep 2022 18:05:34 GMT  
		Size: 276.0 MB (276010039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2026e7201bf75f76cdba4f1cbbf5b9adea773c5a733b4b3bde2ed3fe10f4cf1e`  
		Last Modified: Mon, 19 Sep 2022 18:05:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796d3c78fa8bb8359ab3c5a9ddeec29731beccb8ce8db9efd5baf78f27c65a94`  
		Last Modified: Mon, 19 Sep 2022 18:06:32 GMT  
		Size: 289.1 MB (289080298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
