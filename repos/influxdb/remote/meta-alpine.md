## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:169e9f624104811080443edbf7f8ab978bb927977c31652eef796a849c26cce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6f76863cb06c829dd0f5fd85560e3e7a7cbd5dde014c562fb7bc4bf5805c2bf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26948957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d866decca0f6fdc02095fc5152fab6b9080b7485008d9c8c64b2e7e7f3841118`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Sep 2020 00:58:25 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Tue, 01 Sep 2020 01:00:12 GMT
ENV INFLUXDB_VERSION=1.8.2-c1.8.2
# Tue, 01 Sep 2020 01:00:48 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 01 Sep 2020 01:00:48 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 01 Sep 2020 01:00:49 GMT
EXPOSE 8091
# Tue, 01 Sep 2020 01:00:49 GMT
VOLUME [/var/lib/influxdb]
# Tue, 01 Sep 2020 01:00:50 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 01 Sep 2020 01:00:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 01:00:50 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7279b9f70b385667a52ff20142c09fd4fe94f3c717683fe273d3af53528ada`  
		Last Modified: Tue, 01 Sep 2020 01:01:22 GMT  
		Size: 1.4 MB (1427184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b75bfab31155a561f7b2c6df488ac36d6bd0e8b41b60d5642d4db786e98194`  
		Last Modified: Tue, 01 Sep 2020 01:04:01 GMT  
		Size: 22.7 MB (22723509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eaa71001179a21b80aef6e7e2bec64277ee0b22358785c08ee9e58487b4daf`  
		Last Modified: Tue, 01 Sep 2020 01:03:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f049e96eb066b8724751fc330b5253e828e0c6602da8fee2402306565e15dd74`  
		Last Modified: Tue, 01 Sep 2020 01:03:56 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
