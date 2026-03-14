## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:b00b5baa2231b78e2d7f36eb1a10e2d977f347b9881dbb417b29b6bdf5830a46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:81a969bc16b9858dda59761bd5f64a9e845ca937d25c79bf19a7c2e5ef57d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47996785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0349bbaf083804873fbb03e5d51d6762630274c9fddcd6d18d97809096a67f24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:26 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:31 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68716dcc58a5f148c91121671bed51872ee14024f52511f4f27a30f76dce7229`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 1.2 MB (1225267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a883869ba3b1cd65a45af9359b43f47d6fac6db9e734ab17670747476688a74`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 43.1 MB (43126004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea75516ea6f5fc6e704f8a153c5006c341c6d15af305805fe5621cc87017a79`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23204e84777414408f116926340ada07e4e53fd479fe293933fd5917377c5ef3`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6db343d538c0cd30d0b117de9d02ef0c9964c7ddacb94c1d1548cd2251e8b6`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3cf5b433c5da545ad77ef2c05fbb248e11328258f17be899658ebe11101f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.7 KB (796739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d8831c93eb5116260d6aa262a99b5340b8e251edae29efa3ffb935fd035cb7`

```dockerfile
```

-	Layers:
	-	`sha256:54c781f8f3995af817107aeefcc043140f26364ae6ce15fa46f4f2bfdfcbca44`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 781.2 KB (781229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e179ee50e5cfb1d3f337ad7930775e5df7f00e5978d5acd75cd3102bd71f6b`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 15.5 KB (15510 bytes)  
		MIME: application/vnd.in-toto+json
