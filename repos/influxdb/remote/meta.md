## `influxdb:meta`

```console
$ docker pull influxdb@sha256:eb1275d9a00d3d902dd398f2eff0c8255039191767cea04c0007f41b22500756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:57a044b67fbcc59869345506b2c3e911a8f5f0917bbef96777c10469d6f82d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91924518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b463ccdbb88aeddac659fe2cb6f4bf528d2fa31712966603f303ce742a8c90e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 20 May 2026 00:29:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 20 May 2026 00:29:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231a6a12e39a684b8ef400973532085455b3543f371d1bb90f45442900340a6b`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 19.4 MB (19385146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c88a42d2f3e78083f3422ab9fee7830022e74612847d646975dc0e445f467b`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f6fcdeed90a4e263d4d42f8469c6a2f871ea40910010f73940c93664a9bd45`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6262a32495c2a4fff37a1137f8904b95d7aa4f6d6c66a4190ae73ae7052d82ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517704ae2ac63a1323353df03f5108b0356a0a9eb2898e249df613a4d7cf2031`

```dockerfile
```

-	Layers:
	-	`sha256:0a7f7f23c71460ad60a701c4198a800a0f496f8dd4e1b4cc08f25b1ba5cfea80`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 4.6 MB (4593209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534a176d731bc426208fe21876a10f5f82a0dacb9772e2443aaeaaa1ecc6ed18`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json
