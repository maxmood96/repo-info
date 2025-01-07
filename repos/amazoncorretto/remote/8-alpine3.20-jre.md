## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:1b255c9bcf59c77afacb77ee4b0efefb2f64006a11f5e045998b9cfb71ee4301
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dac900d5b979ba6f75254817b4cd67ed633763fc9166dc993f1f29c04a39c8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45270573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e05b079343a5978b477d87f2a25f55f233e18abf8a8dfe9bd4a876e7065829b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961f5a14c8de2bd0592ceb17aff78869da7d0ed69a1b810056183b189625c2e`  
		Last Modified: Tue, 07 Jan 2025 03:28:40 GMT  
		Size: 41.7 MB (41656574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:376eb1646c8283f793b6bb4c4bfca732c912a27934646ce6a358c80778906dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e496bbfdcc89631caf71eb0597ce76bea831e5ed02bf56e34610adfa212900b6`

```dockerfile
```

-	Layers:
	-	`sha256:4b0da7e4f803540760b2f66f46fc902190477fcefed8f82c03268cfe6a2de832`  
		Last Modified: Tue, 07 Jan 2025 03:28:39 GMT  
		Size: 181.8 KB (181761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4a92dd6abadcd6d4d2c6890c2a95c034c0b45324502b8cab30ce27448ac721`  
		Last Modified: Tue, 07 Jan 2025 03:28:39 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fd033301f2b5203b4a3aa39ca3295b5f57203305a48bafd7aa575c502c2ec93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45445768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e897325fd0d0639d090f158409810d743dbdfe75f51353423278e4199ae77f4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714344b1e7aaa55a474e4cd0c0218363021b0c689041dc73be8432bc4600f3a3`  
		Last Modified: Tue, 12 Nov 2024 11:05:53 GMT  
		Size: 41.4 MB (41358042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8b72c7fd43d1122313aeaa8e6ef45e86654bb88957a45f15d1613530f88dd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a72f30b49fa0f1843cddb79fa8e0d8ab46a87ceccc6a87ea20d31d996458c2`

```dockerfile
```

-	Layers:
	-	`sha256:b02ae8038e9cf782d0f63973d6c43a62d50707a7c7e74ef8b2f1d22fecb57675`  
		Last Modified: Tue, 12 Nov 2024 11:05:52 GMT  
		Size: 182.1 KB (182081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f6f17be0df98960ec5ae9ac7484090e977c230f221737d44391e2f0f1c98d0`  
		Last Modified: Tue, 12 Nov 2024 11:05:52 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
