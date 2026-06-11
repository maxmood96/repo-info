## `influxdb:data`

```console
$ docker pull influxdb@sha256:79bfc29d1272f60c4761145dcfd9eff0a6c2a7842f1868bb364ed32f0181f9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:335b2c7242ff0c96c0ff38835bd4d12f030c70ba78229ae6f45bfd02e531c64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115737703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108ddeba3c5c3d7f4113e78d3aae885caa4877285f8eedf691838bc88f8368f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:28:43 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Thu, 11 Jun 2026 02:28:43 GMT
ENV INFLUXDB_PR=
# Thu, 11 Jun 2026 02:28:43 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Thu, 11 Jun 2026 02:28:43 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:28:44 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jun 2026 02:28:44 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 02:28:44 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jun 2026 02:28:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:28:44 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jun 2026 02:28:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:28:44 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ab958154d8e8e86a9063ad2b71cbfc099c03be2732128f65769bb82ce6445`  
		Last Modified: Thu, 11 Jun 2026 02:28:57 GMT  
		Size: 43.2 MB (43189885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ede7be769055c846ec69453063181a57a50a2486c6b1d7cb2c9c83a6b5ff99`  
		Last Modified: Thu, 11 Jun 2026 02:28:56 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1bb634396dc1c5a9b5cfd7d79cbfd88349395181f32fae4fd1231b5e72ee10`  
		Last Modified: Thu, 11 Jun 2026 02:28:56 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6995857c094f9d39d9b6f5a19e654cef838800d60e7492a2fdc4493c5676633f`  
		Last Modified: Thu, 11 Jun 2026 02:28:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:6742a3ab1caa8050924ef59abfcd925f44ab1eaae560e299ce43398ce9559762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb8e7ffe9c9dd8691bb5dbae577919ff38f1b2f9fae78bdb924853dc8e3e829`

```dockerfile
```

-	Layers:
	-	`sha256:7e558369531b39b435d8ccdef31a11fa577b1a50958344f35c9b7ba293a8bcd2`  
		Last Modified: Thu, 11 Jun 2026 02:28:56 GMT  
		Size: 4.7 MB (4693159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe26b49834172cde5d571a7dbbe2baba01238f754ae7383f44a711f8a444fc5a`  
		Last Modified: Thu, 11 Jun 2026 02:28:56 GMT  
		Size: 14.2 KB (14153 bytes)  
		MIME: application/vnd.in-toto+json
