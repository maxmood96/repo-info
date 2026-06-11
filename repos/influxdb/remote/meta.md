## `influxdb:meta`

```console
$ docker pull influxdb@sha256:f99bbea968f5ac317965cbc216bd2cecf7b6e219c6223444d8c6c4b1116b046d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:9a61794eddd2572bbb0e501c786a37b480925a8b745940c5a755ff8024fa6dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91931757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f6470a35e5487744dd0c47a2227a54ae9a42d9ec06b0320d35b9693cb0c1cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

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
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:28:43 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 11 Jun 2026 02:28:43 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 11 Jun 2026 02:28:43 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jun 2026 02:28:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:28:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:28:43 GMT
CMD ["influxd-meta"]
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
	-	`sha256:a3f85f773931912eeea6112bb0063ae98c1dea5f0b2e6fb4d347f869d620c5c1`  
		Last Modified: Thu, 11 Jun 2026 02:28:53 GMT  
		Size: 19.4 MB (19385146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29559a08e8aa000b38bc73fd6576d9427e715880d1e1edc70f4d1722a1d48c9e`  
		Last Modified: Thu, 11 Jun 2026 02:28:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584fbaee239e60d189bd4ea8dfe6c20de78faf91ff13bea0e119385b9f3877ac`  
		Last Modified: Thu, 11 Jun 2026 02:28:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:d047662228de94c93b013647c041e7e46ddd0952c5ab155e7e6533d7cbb5a1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742eeab9ac0442cc6a749aca10db1167645f13c2f4701683b6bcfe7d5a3f89e4`

```dockerfile
```

-	Layers:
	-	`sha256:51f712059f46067aee759cbda9ac5489644b19602a1c8854832b132b4cd900a8`  
		Last Modified: Thu, 11 Jun 2026 02:28:52 GMT  
		Size: 4.6 MB (4593227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18629c321a3b886b11cbe520d52f285f611ad1901c25832c329900c581e5161`  
		Last Modified: Thu, 11 Jun 2026 02:28:52 GMT  
		Size: 12.7 KB (12664 bytes)  
		MIME: application/vnd.in-toto+json
