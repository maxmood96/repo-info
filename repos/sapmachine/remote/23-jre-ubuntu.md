## `sapmachine:23-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:e0788863d5ae5e104b358df023632b449a44142d0c524bf8c93f1764cd486c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:27db18c3ce5cd8405cdd378c558abc2b02b92616cfbb7111fb81212dc744860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89498655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15295b8e254595072c0c5cf6450982b0a1bfa313a81c4ba714dbd1051d1a6bf3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f96b1dce980c94d61750ebaa44579562dee8b48f2c84680fd97128c938b61ed`  
		Last Modified: Wed, 16 Oct 2024 16:17:45 GMT  
		Size: 59.7 MB (59748292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:86efeca7f7c6ca0513bac13946704b3f70924d99258e3fba9223903d1dead6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0ef9cf1e2c1b960da0f61878293e8597d12589c0e7460d31b44bedd64c1099`

```dockerfile
```

-	Layers:
	-	`sha256:f236f40f01f559383c0ae98565c8f1de33d1853be8a71dc7c4b76c9e60cd30b2`  
		Last Modified: Wed, 16 Oct 2024 16:17:44 GMT  
		Size: 2.4 MB (2366526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fe155cb3e80d95f244707eb92ff0e250bccfda63eaedae99fb910922dbeb8e`  
		Last Modified: Wed, 16 Oct 2024 16:17:43 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e85c3b84bacff42a1cad66da82ef36a7d4eb504c0da8dcc499c295d5ab530e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87696062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654c91bb10a24d86731296749e8b8d2388538d673318bfb8f2b201d04ffc2738`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d3ffada96e867f83df194ef0567d682547cb0a98252d8770bfd870a8747b7`  
		Last Modified: Wed, 16 Oct 2024 04:20:45 GMT  
		Size: 58.8 MB (58810217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b59f6c8b4e8b8e60015630f70c29da913db2e0d5776a94b0674848bfab947b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72a53085195ca67feae2ed504ea4127d48187a74733ff2d2037cc9fe6826ae9`

```dockerfile
```

-	Layers:
	-	`sha256:e6b3cb368e39f01b49321dd0bf1b7497e899e60ec79a81c855a244755528bc73`  
		Last Modified: Wed, 16 Oct 2024 04:20:43 GMT  
		Size: 2.4 MB (2366386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a29f3554ece5730db22a5c0f0f1be9a2835b1b6056b806700ea66d25507cd59`  
		Last Modified: Wed, 16 Oct 2024 04:20:43 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9980edc8b0952ec27ea46352e7380d1f552d6f465a54942436edaee1df52b431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95675418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29be394062d9dd8424f4bb3fc60cb553a397f3834ccb7ca2e262bcf8247ee9b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9b33cda72760ec5694f9cfbceee0a68ad188cda7f5cc4a52ead2ee9416dfb2`  
		Last Modified: Wed, 16 Oct 2024 02:36:24 GMT  
		Size: 61.3 MB (61286449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0157e4fc0b7b4e899c4197d2067b937da4f1cb6bc7da3136f79ce3b3254902f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d221fd7170eae007aec42e66316bef6eac700cd4cb17ea6369e7f82101e789`

```dockerfile
```

-	Layers:
	-	`sha256:74c17eea20576b649be04c6e08bfb23831da7cee18f71f198c2672073b8ede28`  
		Last Modified: Wed, 16 Oct 2024 02:36:22 GMT  
		Size: 2.4 MB (2369844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3cc096d59443095712496e1849247dbdd64aac9736fe7aa46cb29d2d16c4a3e`  
		Last Modified: Wed, 16 Oct 2024 02:36:22 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json
