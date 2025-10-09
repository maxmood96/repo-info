## `amazoncorretto:17-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:f51fc44eeca3752c3e8a57863d6308cfbecc5f19ce4acf6aa360bfa5f90ddfb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eb207f8dcff3761a04703dd83f9079f9b9f8fc37c42fc68d0a8f38981ee01740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149652291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cc72951ecc8daff1e2514b776ccbbc6242083a1ab4456831a04c57edf0d9a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b27aa83763391f0c2f3ed208acdb0c4dd3bd2f5a5826210e8e2b3687376c59`  
		Last Modified: Thu, 09 Oct 2025 00:52:13 GMT  
		Size: 146.0 MB (146025235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b202ea192275160bcd23f4b3adcc98aebd1b1ad2ed73a421f9d2f7ddbeeef53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 KB (387496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1974da9148e89650cdc1a55381062dcde2618ebf25c5577b46293e7ef974ed10`

```dockerfile
```

-	Layers:
	-	`sha256:64d0558db18bc85c08d82f2526af1c10f1d28701cf7533bed7ec5aa25a22b15c`  
		Last Modified: Thu, 09 Oct 2025 00:48:54 GMT  
		Size: 378.1 KB (378079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:799acb2d4b5dab913f142756ec23c03c3ed657f0f6bc9bcbecad451530323bda`  
		Last Modified: Thu, 09 Oct 2025 00:48:54 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e362cb5faf89eee7b90454e15bd00e92c0847984a1f74261ff99cc560b104da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148408941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2757ef74cd894ed602fdf464cf3eab51aeca8cfb4ebcd168c31269ee63ae83be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5cdc925b7604647bffa1b6a42d1c95a85592a1ac322ae3e6a861354c977848`  
		Last Modified: Thu, 09 Oct 2025 01:46:12 GMT  
		Size: 144.3 MB (144319564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f437917883c81bac05ab250d29bcc68ecc5b84393f26cacccd20570eb4467854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 KB (387017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec95481fa14772b9552c120fba7849602b1224e279cb7c260a66bc188e6bbf8c`

```dockerfile
```

-	Layers:
	-	`sha256:bc8f51b07538b6324b2e738307e4bd4fe120aaf2b527a0081bf4b3bf048948f2`  
		Last Modified: Thu, 09 Oct 2025 00:48:58 GMT  
		Size: 377.5 KB (377498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9cd8c1871c0c0d9ebaa132cb0721ad12b8404f210c594a423f980747f63dbb6`  
		Last Modified: Thu, 09 Oct 2025 00:48:58 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
