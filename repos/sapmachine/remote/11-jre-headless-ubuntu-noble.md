## `sapmachine:11-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:8b559cfd6c21426ddab019bf40add7f395a3f7c3db121dafa26d31d2fea33953
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:245b7fa713b6c4f970378781afeda1d9d55a5a81838ec889046a5323863e97e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78949312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c42bcd887dd18c9d674dce21ce64f72de8a31c57d54e8976e6f26a5ff3b277`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e14c21987fdcc9e1cfa199753363d4c4549896a22307ef4759c2260304e20`  
		Last Modified: Wed, 16 Oct 2024 18:59:45 GMT  
		Size: 49.2 MB (49198949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:05372443d0d01435782dc2fd17e74691c2494f439fb83c51bff8bbd74070d7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21674548315ddb7ecbfbbfd081f26340e72121399c1887739630ed441858e281`

```dockerfile
```

-	Layers:
	-	`sha256:0fc225518bf2c1d251ba9cee59367f49f9547f9a02a5751f2f2322e564ad2f33`  
		Last Modified: Wed, 16 Oct 2024 18:59:45 GMT  
		Size: 2.1 MB (2140016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f5fcfca8fc24392357e3506c1926db091cad4f7764eb2118e8a479aef587fd`  
		Last Modified: Wed, 16 Oct 2024 18:59:45 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:eef864cf14c5570540b0b7d3f9c0968f2ea08d0128350deae5ae1ad2973ef5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77402898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e59c0b092a09948eb96a3334ebfcb0c4fddcf4f7b6379e95bf95c6dacd54a81`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442da97e28904f029ab09da4007f47a0efc9989b1ef1e8c94d1a05a2b015f333`  
		Last Modified: Wed, 16 Oct 2024 19:45:14 GMT  
		Size: 48.5 MB (48517053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:110e5495f255642b576bc29beed57b2488c7fbe38e91e295b6c5bc734bffc91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be0a37b5e7cf9aaa5b4a91f480a15f122ffec22e8f2611b918223559fc955f2`

```dockerfile
```

-	Layers:
	-	`sha256:eae645d72ecaaaa9a94c0a9e3f5d7f52434610e5691498aef51a369d01ffdc4f`  
		Last Modified: Wed, 16 Oct 2024 19:45:12 GMT  
		Size: 2.1 MB (2141126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceaddac4637c69331f2b6ae806c8f953188c028dbcd9ad4391eb52ea67749aed`  
		Last Modified: Wed, 16 Oct 2024 19:45:12 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:057ffcda753361af6071cd275059a3eecf58d5617252a1cf4b07e8f3352794e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82108183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2f4e2442d644fdffb4d2c60fec0205884d038d76296ab94e415689ce3e78a4`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:be80ee7bf0872676f625c06a94222712431dc9ebe655627a35406bde59352d5b`  
		Last Modified: Wed, 16 Oct 2024 06:14:05 GMT  
		Size: 47.7 MB (47719214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ab57943bfafe11db1dfaea3b34364697c1c835ddba0eb7810d504fe7e347aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d762ca560850f7a0ba9f37cb6a55533d2381ac1673146a797b55b8b458a9ae`

```dockerfile
```

-	Layers:
	-	`sha256:ca29ec825a154d2cb038855c97ab01fe586d6aa71bfdbe1e3b21ff2cf9a73e0c`  
		Last Modified: Wed, 16 Oct 2024 06:14:01 GMT  
		Size: 2.1 MB (2143274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389d12c99793e46866610345b2595ee2ea77085b727960b7c0d2560c34649a79`  
		Last Modified: Wed, 16 Oct 2024 06:14:01 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
