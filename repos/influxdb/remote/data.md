## `influxdb:data`

```console
$ docker pull influxdb@sha256:be2d5a7bd5ff0644383defcce1f7769ae89363d5867ac5b2615ae2731dcb6c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:0790872efd83e02d8fdd2faf7a2ff410f9ff50a007b58c517d14c783d48130d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117786452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276cebfb7edd0645264657425ddb00bb2bcb80b7dce64169b9281067ebc0707c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 23:04:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 30 Mar 2022 23:05:18 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 30 Mar 2022 23:05:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 30 Mar 2022 23:05:25 GMT
EXPOSE 8086
# Wed, 30 Mar 2022 23:05:25 GMT
VOLUME [/var/lib/influxdb]
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 30 Mar 2022 23:05:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 30 Mar 2022 23:05:25 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff77374c2e1be00d621fbc0713ca958c0ed92607fab1eaaad95af4c82b91492e`  
		Last Modified: Wed, 30 Mar 2022 23:07:17 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edcfcb7a5161abd03b61b6153c6f903029bcfb2d9efa4a6556918c51a064af1`  
		Last Modified: Wed, 30 Mar 2022 23:08:36 GMT  
		Size: 56.7 MB (56709163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97289aef350957936b3a19d68c846a790247f957e99f5d9f0e9c628bc74e2d0f`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1caefc2f0645fadbdce8da95cfbe3bdf21d1712e3d4b95577a26a55d97debc`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fc4496b0657c51da18c2c520e35381f811fe8d8a7eb3c3f4b15209a3b00900`  
		Last Modified: Wed, 30 Mar 2022 23:08:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
