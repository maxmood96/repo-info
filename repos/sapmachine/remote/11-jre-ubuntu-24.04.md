## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:60564c010df4fc577c2db089d6422dd86fedd1a0c4a3f64d5988cfeac79474cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:9461c7f6c2893c2f373a50def6b89e73f478133368575c2b5cc7b1ad55c79342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80091425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0760eca326458f43cd379d8aa78573bb67e1f4422be9058ee799e51e3bfb378a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661385ab8db58106e525a15691730e7d3e402ef5dce940be17c210aa747951e2`  
		Last Modified: Wed, 16 Oct 2024 16:18:10 GMT  
		Size: 50.3 MB (50341062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d0203be95f2278211540b429759e4f368bf660b0f381c1e7ba2adf4c6583ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5bf1b371d3b90cb8a31810e2f4b97110e3460c489e293c79c01896099663a0`

```dockerfile
```

-	Layers:
	-	`sha256:b19ca8c1d1034553e395dd12ed1b5ba2922ac9b835b5d556e212e10f61b3a3c0`  
		Last Modified: Wed, 16 Oct 2024 16:18:09 GMT  
		Size: 2.4 MB (2375477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05f06777bb404f64a042992522615cdc6f9bea281428b511e002dac3989b09f`  
		Last Modified: Wed, 16 Oct 2024 16:18:08 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6fdb1c9d492357a910752025fcfc389cd8e2e74c7b7d8ef4862b73dae3f825e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78567920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac39dd800134bf2e16e3e5ac41c419ea26b54c5b7a21b1fa6d38f7adde0ec3a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded78fd6741b3e9574d5032ca772b0d6b08dec671a6678d095db573c82196a9c`  
		Last Modified: Wed, 16 Oct 2024 04:49:11 GMT  
		Size: 49.7 MB (49682075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d61407d08cf60ae160e38d49a9d7a90af1df3d92cada214e7dee8d9e6d9ba6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b55c44fe65ab9a06f2aff80d28518043aef4ac3be4a7ee8af64dd144e92dba3`

```dockerfile
```

-	Layers:
	-	`sha256:c0cb3a229b9b942dab8c6dd6d716b92ed96045a9b48947987081306183bf54b9`  
		Last Modified: Wed, 16 Oct 2024 04:49:09 GMT  
		Size: 2.4 MB (2376596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528681b391ff61e7898c02d3c6bfaa895ccb6c8cbbf24ea4b737a356823543f7`  
		Last Modified: Wed, 16 Oct 2024 04:49:09 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ff77fdb5e918f4f7b4252b2e5f2f0dd0a8ee8cce80da22862a88f7f56aa8afe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83482282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd01acc64f96ecdead65583c7e80a2974b6c59a2d73a4bbf5fcd164a3a8f832`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0daadcda433b9c6bbe9fe32cac45bf1343c89475b08610efde2d67f7bff65c3`  
		Last Modified: Wed, 16 Oct 2024 06:13:04 GMT  
		Size: 49.1 MB (49093313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9bbecf67a803f59e7eeeee8e6b7daaf7f87de27c900c6fe0c6ff349a9ec110e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296262639ae047ddcdb63fefefbd7103571f993af9eb5223789725b6ac12cf80`

```dockerfile
```

-	Layers:
	-	`sha256:e9ebcd6e5310feabb36b0756d71261b4174d3bf05ffb09e439033ebe7d9de603`  
		Last Modified: Wed, 16 Oct 2024 06:13:03 GMT  
		Size: 2.4 MB (2379432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cb676d71b2da644de64ae49b73e696e2d327382e05c773273bb654ea78105f`  
		Last Modified: Wed, 16 Oct 2024 06:13:02 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json
