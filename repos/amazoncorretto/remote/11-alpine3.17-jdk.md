## `amazoncorretto:11-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:9c034c2e80169b2a992258163e326e8914aea3ac2259bf5efb7fef378f798d94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.17-jdk` - linux; amd64

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

### `amazoncorretto:11-alpine3.17-jdk` - unknown; unknown

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

### `amazoncorretto:11-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d2a58bd960328dbcbd01c01c9f4aa6f05956e889a75c65760183b16ff0dd8c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143306222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4345e6ef6043de0f41e9c81ecfd4c65101edeb6f5471c556b0940ff394567232`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
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
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e706abb018c88377131caa94dee36a160dadf6baa29b1c8fb814669afe3f46`  
		Last Modified: Wed, 16 Oct 2024 20:53:32 GMT  
		Size: 140.0 MB (140031150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dfb390cd60d37241a49ec2c23fef84b9a168f3c1a116759f292378152344ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 KB (396339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4ede7cfff75e914d2ef25c876e3418d69be212b3ba56afe48a3ce944d898c2`

```dockerfile
```

-	Layers:
	-	`sha256:2f8c34792ac460bda909d2575662a52531573879fb0322a0779cd50f085702d4`  
		Last Modified: Wed, 16 Oct 2024 20:53:28 GMT  
		Size: 387.0 KB (387031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348c40f9c5ab97d3bfdb5271957e99ff539e68ee36a7f8a320a4805e0d545dad`  
		Last Modified: Wed, 16 Oct 2024 20:53:27 GMT  
		Size: 9.3 KB (9308 bytes)  
		MIME: application/vnd.in-toto+json
