## `influxdb:data`

```console
$ docker pull influxdb@sha256:c47990ad54cbab2c4b7ce6e5e34b87d517d46a6323f9bfc8abda198038602a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:f7e31854dd0ffbfa5ef8ac02df3abcf90ff84e89fff55ae0ceb82c4dc6208d16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126810142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076db8957be42f4ddbd11be5d3b3ae5c80792bb2f5c5e547779208ccb54e9396`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 22:08:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 22:10:06 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Wed, 31 Mar 2021 22:10:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 31 Mar 2021 22:10:13 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 22:10:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 31 Mar 2021 22:10:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 31 Mar 2021 22:10:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 22:10:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ea2dd79e17761ed8d11e98f7420d9d909dcbc0ca1fe34ad492f5e495302a6`  
		Last Modified: Wed, 31 Mar 2021 22:12:05 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d41b7827948e414f042e1b9178e16f0fe855f9c0a2043a884762561ebcc529c`  
		Last Modified: Wed, 31 Mar 2021 22:14:56 GMT  
		Size: 65.8 MB (65796441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd72595d8d8e4975ceb4c2dc6f49bd4d712750c83b2ea0306138ad9367dc582`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd848f72b95e08bf0cad39dc3de90ba4fa88364406a9f418c8ee9dfd2faf08d`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1657f716309bf8a123806bff8a8b445f5ed98211006d7fa2e159d9ea6a02b0`  
		Last Modified: Wed, 31 Mar 2021 22:14:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
