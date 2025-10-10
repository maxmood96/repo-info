## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:eac102f852e250ea715054a95bb0e678834f0a55f44696bbbae02c7318c85837
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6de2764f5b5126ba312ede41e8f8d9339ae43b51331dbfb0584afb19e7e7627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33392907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd38d6a5bd761486d09fc84992301354d427fe85c87f80707b92379e9afad9b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054a58c55d36caa7fbf407b8745351083d7c05a69a7e6066abce1135ea0807b`  
		Last Modified: Thu, 09 Oct 2025 21:20:34 GMT  
		Size: 3.6 MB (3562955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65619a8d185f5dad1aea15677d27f2e654fbf4acf615ae121e45b4396d48e63`  
		Last Modified: Thu, 09 Oct 2025 21:20:34 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa30bd830b30526609a60c1a2b2348cbd420535868f51429ab9f7eeccfa7da47`  
		Last Modified: Thu, 09 Oct 2025 21:20:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689834fe3549bd5921510f05250a4f92daa6717930609a50b795fd7cdb060ebb`  
		Last Modified: Thu, 09 Oct 2025 21:20:34 GMT  
		Size: 103.9 KB (103893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c805d5f0d444561afed793274af3264abb4f24dd957c68f774df4378f6f55aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d7a267164eea35d703f119a364491d1ba1749cf185b3e6f4f6ae4e6566399a`

```dockerfile
```

-	Layers:
	-	`sha256:fe18de2c1dbde40b129bc526fb61505c28dc622be275dc9ae36e4aa5bde5da20`  
		Last Modified: Fri, 10 Oct 2025 01:07:34 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d88bcad2c78b2093f6a920970fd535c131386715cd1d9ac2dc361b9713e8f13`  
		Last Modified: Fri, 10 Oct 2025 01:07:35 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b6607d1c1f26a2426e5dccaf8b1f3ad11ff71868aee2a7644975a8e9ea6e05e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6e4bc4bc47cd32cd34bb72f34c43850881b8e067fce3e33e727d1861f28852`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c2f690de8709175b326a45f5e6fb46bd6b1f8637f5aec3195fd70de5ef2946`  
		Last Modified: Thu, 09 Oct 2025 21:21:39 GMT  
		Size: 3.6 MB (3561234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b7378bc18a20662277791fb8d23d593d2f1a5c147001e888422944e80f93d`  
		Last Modified: Thu, 09 Oct 2025 21:21:38 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2362c88af7067bf08c69babbc3f3dca0b26402b831fab85dc17b221500a82e6`  
		Last Modified: Thu, 09 Oct 2025 21:21:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3351b51eeba9456c22fe429d9c371b3ca7a49f02865b37cd2737d07c403913`  
		Last Modified: Thu, 09 Oct 2025 21:21:38 GMT  
		Size: 104.8 KB (104773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84a0c8291a3f87c5280ad4f23e193892e56296717dd2cbda9635952a6af35266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0366648cccee4700584faff1a26cf540556761032bc92571e75ae1e6ee3100`

```dockerfile
```

-	Layers:
	-	`sha256:a8754644032419fcafb9a6484fcbb14142e8dbb013cebdae08bdc533cba1418f`  
		Last Modified: Fri, 10 Oct 2025 01:07:39 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:747937b79fa66ab8648c1a047d1f7a2f169b2c4eccbd211e325407dbed4cd905`  
		Last Modified: Fri, 10 Oct 2025 01:07:40 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json
