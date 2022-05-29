## `influxdb:data`

```console
$ docker pull influxdb@sha256:80d1447e23194ac263dc324d567eaca3cd7d8c743286466eb403a193be76806d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:f057b9826c94f3cbffeae1559f46aa7d57e11d4313d620ebb2b8f3c03de49aba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117789479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e07f37814d7711a17b11ae3b7b0c2494ddd56c77a1f31560ec99d38cf733e6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 May 2022 01:22:09 GMT
ADD file:ba5db69738244d00088ef591ca43fa8b3189e78fba56bc69b70a232e6f04c7e4 in / 
# Sat, 28 May 2022 01:22:10 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:44:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 May 2022 01:13:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sun, 29 May 2022 01:14:07 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Sun, 29 May 2022 01:14:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 May 2022 01:14:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 May 2022 01:14:13 GMT
EXPOSE 8086
# Sun, 29 May 2022 01:14:13 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 May 2022 01:14:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 May 2022 01:14:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 May 2022 01:14:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 May 2022 01:14:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d3d4e1d44a24e0c5abd41b803d14f211ba153bc7963871713cba8ee5fc687888`  
		Last Modified: Sat, 28 May 2022 01:28:41 GMT  
		Size: 45.4 MB (45429730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec8bceb2e238bbbbec9e458cf83c1342015ed1b717be0f88b50d267c52437d`  
		Last Modified: Sat, 28 May 2022 02:52:34 GMT  
		Size: 11.3 MB (11302994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2aa521faedb4a16c079e9574f537b51a05c2ad4fbabd16f83d9bd58c365bac`  
		Last Modified: Sat, 28 May 2022 02:52:34 GMT  
		Size: 4.3 MB (4342992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386debe6a9999be3c003f19bc8848d062480e60c05f846d134e34cc9c606e0a5`  
		Last Modified: Sun, 29 May 2022 01:16:22 GMT  
		Size: 2.9 KB (2852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97197a056b127568e26d51e8dc0b1726ec9dac509b9c2e7de161521dffe9f`  
		Last Modified: Sun, 29 May 2022 01:16:47 GMT  
		Size: 56.7 MB (56709134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0d2f38f0f0cd00842c355b2780895a8dff3d698baf794162c142ae4301837`  
		Last Modified: Sun, 29 May 2022 01:16:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b4717d882bf2ca3662fbd88b6cb429c8cfc1002675288fd52c7dad654bfb49`  
		Last Modified: Sun, 29 May 2022 01:16:40 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db994e43254a59c721f524e5585b89f7b7efd529dc94349c11eadd14216f4fcd`  
		Last Modified: Sun, 29 May 2022 01:16:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
