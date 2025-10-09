## `amazoncorretto:11-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:a927108e26bb7f390f3ac7c7ba15efbd8a9808ce9104dfa6c5fbd1f80c28b47e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:512e6ba666bee57cb60ac0deb57962a3518afd98433474251560495a9df62fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145713007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb3f79744a99276afc003c27dc46cbe85d1702e8ee73d73a7621bf4dd817e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:445bf25b027825c7be67aa0e47b5bb0318547ba438521111d5029a9e8d545557`  
		Last Modified: Thu, 09 Oct 2025 01:35:06 GMT  
		Size: 142.1 MB (142070438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2ff7cca60e4bc752eef8234df71b35b8e3c7766628e26f98484d44deb4dae4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.2 KB (400199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd71674c1dff55b763879715d983c755755fff2e3a7af65574831e83b531b59`

```dockerfile
```

-	Layers:
	-	`sha256:5e1cf15fb5ed8f04799adc54237ef42ca1174eb6cb123e863432aae581b03388`  
		Last Modified: Thu, 09 Oct 2025 00:47:55 GMT  
		Size: 390.8 KB (390782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90d89c04713caffb2998f4b259e272df81c5968e8d04cd19aa51056782e4dec`  
		Last Modified: Thu, 09 Oct 2025 00:47:56 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75b31daf7c12a4e89898826b213bdb8c0c6aeeac271152a37210899dbb89f3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144234426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0c8cd5bc849c51d95c9b12457fc66a4648a755128452ddfaaf431a2464d0df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:f4a70d36f204cc20d5b28ac2adfa5550b4405b71ee5893107d9f63c36f4aebe9`  
		Last Modified: Wed, 08 Oct 2025 21:46:52 GMT  
		Size: 140.2 MB (140242073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:af2e41c7c7048f8cd850ca6895f1d78ce7d5e34eb843a2451de310049b15d2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 KB (400359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bde6cd038ee9d82ff3386e433f705defb0048150b5a4a224ee06608bfd689`

```dockerfile
```

-	Layers:
	-	`sha256:78fd775b8095f10d79c4006c63b9b34d642fd7839e320b57e8028c6d9ddb33b4`  
		Last Modified: Thu, 09 Oct 2025 00:47:59 GMT  
		Size: 390.8 KB (390838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1be9cf3803e677071f32e6814deba2de020a5917e979913684534c1b02d568`  
		Last Modified: Thu, 09 Oct 2025 00:48:00 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
