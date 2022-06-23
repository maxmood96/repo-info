## `influxdb:meta`

```console
$ docker pull influxdb@sha256:22802a6c409c5cdd3bc054c2196b8320041e1be81dfa4683d21358cd832113d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7ecfdafa61c3d2d3f057774038cf7c870861c9d1f094abb763bbccda889be0fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84496164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095bfff223c443c0e87ec288f1462d1732302060b304b9799c4b17ae4447e1b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:10 GMT
ADD file:4c5e0bec5f780d9c6bfbafcb9e6ed641781dd7f7c2853a0c49d6613e9fef9516 in / 
# Thu, 23 Jun 2022 00:22:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:54:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:54:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:17:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 15:18:14 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Thu, 23 Jun 2022 15:18:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Thu, 23 Jun 2022 15:18:30 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jun 2022 15:18:30 GMT
EXPOSE 8091
# Thu, 23 Jun 2022 15:18:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jun 2022 15:18:30 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jun 2022 15:18:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 15:18:30 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:8372a04f222be82bf67eb0010a59644b1e52f1246b3da9034edaa98f3d591cae`  
		Last Modified: Thu, 23 Jun 2022 00:29:36 GMT  
		Size: 45.4 MB (45430020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1728fee80d376293a9ef5fdcc0acd3f6398fc4159b12064ce4c1e66f67e7e9d`  
		Last Modified: Thu, 23 Jun 2022 01:02:01 GMT  
		Size: 11.3 MB (11302923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cf50aa0a4b80b39d1bf4be232d404da0b1ad38cdd3bb1a017b727947b5f4bb`  
		Last Modified: Thu, 23 Jun 2022 01:02:00 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86e15a947f1f4c2ec5261546aba1007d9944f87c77bed2eb2cb9f38d91fe491`  
		Last Modified: Thu, 23 Jun 2022 15:20:31 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d7551c1766386d104f430be81f49cfaa95686138d88c7038f7e6cfd1e66f4c`  
		Last Modified: Thu, 23 Jun 2022 15:21:14 GMT  
		Size: 23.4 MB (23416877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535fe8a7786b0b29380c8643d4e5e61e5e5017afcfa08a3b8af6742f09dc3a68`  
		Last Modified: Thu, 23 Jun 2022 15:21:11 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa9e12f9123b3fb169ca58d9afa4152583f9f5531c26fa69ce35b5e7ec63667`  
		Last Modified: Thu, 23 Jun 2022 15:21:11 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
