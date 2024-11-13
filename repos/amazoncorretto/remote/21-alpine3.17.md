## `amazoncorretto:21-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:6ed399441760d860717318db95fc50846bd0173145ec728733e69b782ead78e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eacc10477e9a7f76be5fbcb2369ae69bfb0b5e5ded5405025632c3d58f2ab8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162321737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ff34931bc2b197a6ca0be548d8cc3eafc13861547bc6412cc292a7a8686b8c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:dbddc550d1bc979dc6510515fd7d1dd1aafedc9f168f9b6b34d4022b55824571`  
		Last Modified: Tue, 12 Nov 2024 02:12:26 GMT  
		Size: 158.9 MB (158929485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8685afb02e2ffef310dc94b3ec070ddac89697389a3a587da0b0844409620504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.6 KB (389574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59440c77b1147e1ad9668fda4174ef9de09acd73d478cf1cdff884b92fa816b4`

```dockerfile
```

-	Layers:
	-	`sha256:1aaabfe57788d53b61243e0cdc80480d45391e904eb0071b367a8fb961f9e57f`  
		Last Modified: Tue, 12 Nov 2024 02:12:24 GMT  
		Size: 380.2 KB (380159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b32116124ca3a300bb94728db2ebfa2e278aa4d4a181b62b4b215a46b46d7e`  
		Last Modified: Tue, 12 Nov 2024 02:12:24 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b24ece0b54533a2b60210064c12d1065ee890d6c425dded6265082ded2d9e557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160153743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0b9237a839f9362541a902927626a890f4a15655985f6a842e44164464e329`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:897a8147dc8ba04506a6bd28aee0d6fbc3fb0be6fc689fa9d6b5b6b7f1934e43`  
		Last Modified: Wed, 13 Nov 2024 09:37:35 GMT  
		Size: 156.9 MB (156878582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f7ef696403a4ffde9d2810bf2858e066e7429bdd97b89c77e34e55f64c09752c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967c85de3740ecb8c00b44727d6815f121628585a9047811c506a43082ff75e5`

```dockerfile
```

-	Layers:
	-	`sha256:eb7ed6a2ac9fca4b3f575befd8f8adfe8dd8598ad127bada6995e009ed1ce36f`  
		Last Modified: Wed, 13 Nov 2024 09:37:31 GMT  
		Size: 379.6 KB (379577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f259b1022b0c9f0b123fac3cf23f39f84aa577f3a0ecaf35cbdc98bf42af96`  
		Last Modified: Wed, 13 Nov 2024 09:37:31 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
