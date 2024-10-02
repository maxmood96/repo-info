## `sapmachine:lts-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:ca57f478630bf123f54bd923a15a60b20ee706be00e759e6cbed6417af68a337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d89374aeb0c768674dd748cfba92844df23adbf424b18ff698ebf4a6793af45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244152868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c26222dba8e432f747a8b969edbc9a8b6d2317bbfa521d7c6bc35e99144cb0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26200f952fd0914664564df8cd1e8afc1a270a6f16b4bbc7d7576e9b2a380a1`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 214.4 MB (214403008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:74ff0ffa77b475849518eb086ef51016158d3c41bf4f2543fe5e53c988c645cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842afb85074675387ed4711df678d57d50a83eba8b8104c3ffea3ebdfcd7f692`

```dockerfile
```

-	Layers:
	-	`sha256:7ca77c87039eb924d019454710bebbddb89060873b64501c7a622e804f3c2ab1`  
		Last Modified: Wed, 02 Oct 2024 01:59:57 GMT  
		Size: 2.2 MB (2213267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b91dd775b5142428d1f99c632e34118700496dbc9d859d24e0ae4f42196d3b`  
		Last Modified: Wed, 02 Oct 2024 01:59:57 GMT  
		Size: 10.4 KB (10402 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:32568d4cfe3e95c7281053887c87adeeb3ea5af88d7da6ad3f16af07dc945dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241388247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849fd769a4e2f295fef5e4ad6281ff09bc7cf668f9a183d1b081325f2d40b601`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316c1983efdc3b35f0d98b98d79e53eb75b56cd6a3067c09ff9a8f87ddc3c6cf`  
		Last Modified: Wed, 02 Oct 2024 03:50:45 GMT  
		Size: 212.5 MB (212502817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8e262e927529cde1f960bf58daa1d2e03882cfa86bbf46826b7ae5c31206b45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5ac04c0b8590f9c3bbecefefba9c24aae709e1a186ead72b8681b3c6483b01`

```dockerfile
```

-	Layers:
	-	`sha256:202ab4711a270df163c8684a4c1be6d8cc8c28a6e4ef8e243b364bb10ba7700f`  
		Last Modified: Wed, 02 Oct 2024 03:50:40 GMT  
		Size: 2.2 MB (2213785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f49b6e52c34d3407c380c9b1333105c5fcd5e2b4362f81b9e4e5ffa07e92ac90`  
		Last Modified: Wed, 02 Oct 2024 03:50:40 GMT  
		Size: 10.6 KB (10561 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0b857944f58f7fd2aec33734a879ecf9e3b732b4941dd8d242bf391cda20b78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250062119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1312b39f5ef20b3cca060cfc0992d79ed509fcebec6592650b5e733ff9e46af4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ee18c5fccdde760459aba4ff1e9823ec3951985353329f8dcde304813d149a`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 215.7 MB (215670098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6f52aa8ff25c2b384e611e0296fc74b3e17194909bbbcd4f95b72f4daf8ce57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2225693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2136bad501cb978a6dc57ba4325b455326b34ef29eb3b7f1c61d9a38487259f`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a0b56f00cca56869d3dec27c096805987b52d42a2201e44463e89cde9adad`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 2.2 MB (2215222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d274ab969379ddf8d9ac049e85cb429ae0ab3af862e512abaff4f783ece6fa5`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 10.5 KB (10471 bytes)  
		MIME: application/vnd.in-toto+json
