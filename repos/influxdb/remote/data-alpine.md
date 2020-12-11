## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:1c87a9977d2fc65671852b1b5c31e70534d217262d7f415fa98b12d94fe4ceee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3c345f2719cd0e36c1974cd4ac409bac8ac849f06485f45a58b3a8fb73c66608
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69768139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053ef724bc76312772b2a367cd762f35b7506765322fd97f1c58cd55b5f7ccc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

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
# Fri, 11 Dec 2020 05:59:14 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Fri, 11 Dec 2020 05:59:15 GMT
EXPOSE 8086
# Fri, 11 Dec 2020 05:59:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 11 Dec 2020 05:59:15 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Fri, 11 Dec 2020 05:59:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 05:59:16 GMT
CMD ["influxd"]
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
	-	`sha256:a1a30a42ee9180ddc3113a2340beaf2640f180f3b931c3f518e8f43e08d41fdc`  
		Last Modified: Fri, 11 Dec 2020 06:01:37 GMT  
		Size: 65.5 MB (65540957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43037875c9114dab7ac19a7706f707243f179b6ce6747d222e3360be4610839d`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40d1d20fe9c8f9431342c512b83d826b544f5955642d96e09c6f25de99ff4f1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85e4ac6ecf6b434790c5db134b171788aca3e40ed6abdb98066007274e608d1`  
		Last Modified: Fri, 11 Dec 2020 06:01:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
