## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:811bb74fd47fc8488e9bb56e98ec6fe04f53089340529f71009ba8174333da52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:682ce0779451e11baba116010e94fe6b719392a3ea9f225e7c366fc5a41a06c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104651413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c892a03a2a1a6fb7ec935bbb74f4de56c67de59c6e93e81fb2b2afa15573f2e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:09 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:09 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228516198dcf71bb7973cf0e588a55b084e664ca989f408ecf3dd4a0ff9f028d`  
		Last Modified: Wed, 22 Apr 2026 21:33:25 GMT  
		Size: 100.8 MB (100787224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3fa1d9e5973e82f40260eacb89f43534399281cc69e29aac2c000135338e7fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 KB (258346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3103340ed0a97ee1756756ce48b5742d1860d6c1504b26e2513c555a9b5f2d`

```dockerfile
```

-	Layers:
	-	`sha256:c470dd6fc6e1fb3061abce4f4ba0a4c7e8d500e374685c6ae86aaa1eca6dba50`  
		Last Modified: Wed, 22 Apr 2026 21:33:21 GMT  
		Size: 247.7 KB (247693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605704d4cc86480ebe9eed29ca2b8a64665e431871998e3b11ff7c4a7004cb7d`  
		Last Modified: Wed, 22 Apr 2026 21:33:21 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5c8694439c7e23eb1b8d0c4b43971ddc048ac8e296426167a071d2b35f8b80a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104771394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a94ca26763c9afc7191f236cc4666206490db5e5de7f542df53d2793aec85e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:16 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:16 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:16 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce3fd15c9d9eafd7fb5c5782c31fca73f6c459593a4bcb43e6b505a41d156d`  
		Last Modified: Wed, 22 Apr 2026 21:33:31 GMT  
		Size: 100.6 MB (100571524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b547a323a54528a4969bd027ad7138f92aeafd61d81a90f48a413f1249634d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 KB (258028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8c56043b03cafa9a14d2a8fdff6cdbd557912686b1e886bd74804da8fd57f6`

```dockerfile
```

-	Layers:
	-	`sha256:fdda35329d5692bd79602748897dda80f66632f4844e7141055d52cc5db27b61`  
		Last Modified: Wed, 22 Apr 2026 21:33:28 GMT  
		Size: 247.2 KB (247223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b20ad1b308b71257911d88fd6c2e5184c953dedc244fc6c6954e511a85e795`  
		Last Modified: Wed, 22 Apr 2026 21:33:28 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.in-toto+json
