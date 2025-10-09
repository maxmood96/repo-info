## `amazoncorretto:25-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:35cb26e5d69bf7314f4e28cf180fdb2a75fbe3cb883c3673110f5938640fa11d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9fbad741159710f888fcbe6b3dc2d8b1f8af3097e519c8aefbcdeabbde164ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182168079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfa7484903e60b4cdb49e493d0b30e2c443e03c1f79d49795d5208acdb4c9c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7112510ed6002a99fd6deb9664c03f74fc2ce55fe582928339e87233276182`  
		Last Modified: Thu, 09 Oct 2025 01:41:51 GMT  
		Size: 178.5 MB (178525510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:317987aaa28166923dd68ad85f60d1da9878c7682de79c8ac3dedb9d334e5e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 KB (402390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39817400c8d87d3dc635f85ea7e3417086db8974382c2f00f0bcbfcb4624cbcd`

```dockerfile
```

-	Layers:
	-	`sha256:8d260226b57296bbe4b0942d6d0534e253a072a973261542d079fb0a03f4ac5f`  
		Last Modified: Thu, 09 Oct 2025 00:52:18 GMT  
		Size: 393.0 KB (392975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec0ff8dd0086ec5d46082eff757734eb4ed19f29501ca6a468f54411f28801b`  
		Last Modified: Thu, 09 Oct 2025 00:52:19 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a3193ad2319a0e07c8cb9e4960c04ad50f21023d567b670e82cafc06064f257c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180064942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35428868706f1ffc4b9af9711aaf7cf942591c6fc32380fa4001193cabf2d27e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e66170d1eb274d5369fdee948b58ca8ef9d6da121abaf8b0108392006d6b11`  
		Last Modified: Thu, 09 Oct 2025 01:41:53 GMT  
		Size: 176.1 MB (176072589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4a455429fba36aef3f780a00810c43d1210468a10ebec725040fdfef824621d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.9 KB (401910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb73b6233cb130b6319f5007bc8acf27268ba3cfc4a1dc0b62d520c2f27b088a`

```dockerfile
```

-	Layers:
	-	`sha256:5ca9e9425a3ea099fcd1c78ce8c80cae005abf0a0b4926f815be2c57afd66a1b`  
		Last Modified: Thu, 09 Oct 2025 00:52:22 GMT  
		Size: 392.4 KB (392391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab2bc2830b878419eb6512e8436a23fe7fc71944dd2953620086ad89d12fc2e`  
		Last Modified: Thu, 09 Oct 2025 00:52:23 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
