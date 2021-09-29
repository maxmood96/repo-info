## `influxdb:meta`

```console
$ docker pull influxdb@sha256:90906c6d330994eea9544c45fd9f3eb7497921b52c04a8751f2d59e04e78d445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ab5994bbcc2357ee2f14e4421b7b4f2a1e8145b95453a428539418523ee6e8d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84440108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcc768e2d62b3d4f3c378bab4604c42997085bda2bf7c63a17465cfd7152ddc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:54:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 01:54:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 29 Sep 2021 06:26:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 29 Sep 2021 06:26:58 GMT
ENV INFLUXDB_VERSION=1.8.9-c1.8.9
# Wed, 29 Sep 2021 06:27:17 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 29 Sep 2021 06:27:17 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Wed, 29 Sep 2021 06:27:18 GMT
EXPOSE 8091
# Wed, 29 Sep 2021 06:27:18 GMT
VOLUME [/var/lib/influxdb]
# Wed, 29 Sep 2021 06:27:18 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Wed, 29 Sep 2021 06:27:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Sep 2021 06:27:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea40d27a2cfcec3d38b2a0ebe5ca77633d27a394541c449b500fce4639516d4`  
		Last Modified: Tue, 28 Sep 2021 02:01:24 GMT  
		Size: 11.3 MB (11297892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523d612e9cd24c2fca3c4d97b340e89c7dc6bb326a9d75d5a0476f56680d06dc`  
		Last Modified: Tue, 28 Sep 2021 02:01:23 GMT  
		Size: 4.3 MB (4342401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7664c6d90947b8b4ab65e0ebad116c3c01dbc88442f8c45245e5fe0c22431ca`  
		Last Modified: Wed, 29 Sep 2021 06:28:57 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffb9fa2d6349b25f365e3ab8eaca8eeb07249730f4604d43f9acaab518855c7`  
		Last Modified: Wed, 29 Sep 2021 06:30:36 GMT  
		Size: 23.4 MB (23416741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67372d76b5daf16afdf096da9d76e0e75635926b6b600bfc4a5fc3e2392acfd3`  
		Last Modified: Wed, 29 Sep 2021 06:30:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2ad1f52ec93004934f7a694c2f36c30327f72cb1296bbee60ceef8df81355c`  
		Last Modified: Wed, 29 Sep 2021 06:30:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
