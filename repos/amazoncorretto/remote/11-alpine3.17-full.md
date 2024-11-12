## `amazoncorretto:11-alpine3.17-full`

```console
$ docker pull amazoncorretto@sha256:0f5fa40b2a9524e24a883d3d709e32b5ad5294ab56ff79109777d69af6fee850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.17-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e970565b698bf6e2611fb6bb572d1e16c515a84008922b805c85b2e356eccafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145302656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b16025feb5479a30786c9deda3d0dab9286cbbadb5142a24c42dc0fb15b7f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4253d06ab35572ce3c9a5d11a5d93eefb15c6bc795fddf0bcfa221ed1a43dae0`  
		Last Modified: Tue, 12 Nov 2024 02:12:03 GMT  
		Size: 141.9 MB (141910404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:94f78b99af86290523f68054784f55d4377c8c31f901da7cdd8118a8ad216469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48907d323d2dfefef2a4e50a31059a855496309d38384fcb8eec35532f52a8db`

```dockerfile
```

-	Layers:
	-	`sha256:9db82120461be239efac52e727aea4a0cd11b0cab847ef37c50da1790bd02f41`  
		Last Modified: Tue, 12 Nov 2024 02:12:01 GMT  
		Size: 387.1 KB (387068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915aee020d3c6637c94ef43cfbbcb39a63f5d56ac3e921d659ae35ceb1404bbf`  
		Last Modified: Tue, 12 Nov 2024 02:12:01 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.17-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:420af9722aba26fa133029b29c888972bfb3ecfe1f137efec71d799aeb591907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143306394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fa755b76f7d82bf13d4efc3a98596c72ae052a7cbf3618514479c716e85a89`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:61254a502902280aa7caa832f8b3ed5c96aa04faf42ab0ba23ff17638f910f21`  
		Last Modified: Mon, 09 Sep 2024 07:02:02 GMT  
		Size: 3.3 MB (3275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c64773b2a67b19b6739de68ced2490659277cfd1c1aee8e33717634a5f8002`  
		Last Modified: Tue, 12 Nov 2024 11:06:27 GMT  
		Size: 140.0 MB (140031233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:733cd083cbc6d201f1abe5db46a8f057bbcb577602afcd4a675ac7efcc81916d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 KB (396645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcc55d5bbbbbfe1b1ac622efd1e56358e98de28085e8a3a359e892175c6c2d8`

```dockerfile
```

-	Layers:
	-	`sha256:2c3aa55fdbc7c0e08639a13ee9284a2f253bf91502d64c47c35f811c024a97f4`  
		Last Modified: Tue, 12 Nov 2024 11:06:24 GMT  
		Size: 387.1 KB (387124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dff083e75c2cd137307be9b167e9a189fb0387b55655bf4f93b410fd5f5692a`  
		Last Modified: Tue, 12 Nov 2024 11:06:24 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
