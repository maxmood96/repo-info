## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:aba45952ba793deaaa74101d0c0e202937ca2aa1ffdeba836f15f16a4f2132bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6de36161d71b004db9cd31ad612af158d39191aad0c2a1d0693c2fccac00f46b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26961458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f43fb7cf000ae30a9a8e8f3ccb602acb3c89a831a047dec2c0b597c972603`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 05:57:55 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 05:59:08 GMT
ENV INFLUXDB_VERSION=1.8.3-c1.8.3
# Fri, 11 Dec 2020 05:59:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:28 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Fri, 11 Dec 2020 05:59:28 GMT
EXPOSE 8091
# Fri, 11 Dec 2020 05:59:29 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:29 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:29 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16278230bdd89f4300bb64c70f52ab02811e9fb441099f76f89267ba46b906cd`  
		Last Modified: Fri, 11 Dec 2020 06:00:06 GMT  
		Size: 1.4 MB (1428310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439e80f23f5fdb224b0e548ff276d0fd87d74ef07d5b9331e70ff1a95114e118`  
		Last Modified: Fri, 11 Dec 2020 06:01:49 GMT  
		Size: 22.7 MB (22735481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f624aaa254c210e8f87b8be506925d54e7ce9dfd01210b97a72b4c1ed11b79`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87faa02d0b3f3414f42ecf87842e3d2782294b5ba32a2e001c0495e02988cff4`  
		Last Modified: Fri, 11 Dec 2020 06:01:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
