## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:7927e75db5f316e37c3113b5177a6fa8681d7391a96618c088ab15787de4affc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:aee9351e25ddc560646525e557b534ed749f80efaa05669cc166bbd844436c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60256387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c939edf22c661b04f3092556641ecaf6d8b92243a08ee378530037c3f85f514`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7671d30ee0069a32147537eef1beaae52a71b59148743b8ebecaf97652901808`  
		Last Modified: Tue, 21 Oct 2025 00:19:29 GMT  
		Size: 49.8 MB (49759136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e69a5781d8cd1c4f658f0b3f68c20304a5fd8a859a9c6dbdb1259781adf17d4`  
		Last Modified: Tue, 21 Oct 2025 01:48:19 GMT  
		Size: 10.4 MB (10404089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160595488c3b8bf91696f3563c9ee88afad2d590a134017c8aa9225194a9f86d`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddecce8bd5b772afd009ec389c35f5aeecd6983116deeaa837097f9b48a2334a`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a96bd959bafb1ba81532e3adc8991755d2dfffbc021c13c7ec34e6584d3e1`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 89.8 KB (89809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71cb7638d5f5a793ce3760e7f92bd0fda11a63685268bd6240ab9b806233ac`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1513c91b584b50c71e8b83d78ab0523e6fd6f81a3b2c750241106fb8fbab518a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7842dc971b9d165db9867aef593bddafba7ce33b098d0af5d5c3d7c47a992d`

```dockerfile
```

-	Layers:
	-	`sha256:4b5b1a9cbea0a198035bb719c86fdf528f2692908cf3c16babb1677fc9015d6c`  
		Last Modified: Tue, 21 Oct 2025 10:08:24 GMT  
		Size: 3.6 MB (3603836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0980687dd2d414c5d8866441fcdafa8ac37e213ee04e955abf019dd18c44bd9`  
		Last Modified: Tue, 21 Oct 2025 10:08:25 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f084cf3d6a9acbef72753173539373c2583fd7ee487ddcf14f609e888025fb91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60165538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e664a348864ee0ae599e346f1d71b96bf7079e0f929c6d1e25e56e11c558d4ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f6aed6c6f2efe803974216c59eb03806f2c41bc69dd9196f4b2f7cddd7e58f63`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 49.9 MB (49888482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95495915d6e89c63dbe5c48ac80b1a01a228ae0d48d8cb9d87ba9f8a9503ca78`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 10.2 MB (10183242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3304319a9c5fe0dd0ff225c24e2a44dacb6188bf8793c972033aa2395d6f44f7`  
		Last Modified: Tue, 21 Oct 2025 01:52:26 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e93ac009827fff09a62d06ee8b2b51164f282a268db4481b43c1a08e376fdc`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636300d427cb1454cb0c7b7bb2f30a23ece8d2aee636ae991b8e4d8d14383bd7`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 90.5 KB (90463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94b5cf98da4cf063bec89956a2ae2c5f11b8350136ab559802cd0d7543fbc5`  
		Last Modified: Tue, 21 Oct 2025 01:52:27 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9631f6604aca6507aa45ff646ce6509568b6324e7f8b2c706bb99dc95963c0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debf832bb0c5ffcf76182ca4ad37277e52a22fb0284ff829b7065c740438e7de`

```dockerfile
```

-	Layers:
	-	`sha256:9913fc5cc6fa511506e8108618d1ba5d65c28bf8967db5a193863a4e527bebbf`  
		Last Modified: Tue, 21 Oct 2025 10:08:29 GMT  
		Size: 3.6 MB (3604713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bee563b2ee76c3db211b8146611708943bffdc80121ed5d3253020c1a5ac89f`  
		Last Modified: Tue, 21 Oct 2025 10:08:30 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:18b4a2d5c2ea6c5c9a2bafb43f5311a4ccff19b71924423224bd2e7ff16965d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61782555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17428c1e42b56296c3c442c2d79d4b28f0ed43b41218dc469a34fda9424320dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bef87153a80d12c20903cc117b0638354009942edbd8ed3d2109a962622491ad`  
		Last Modified: Tue, 21 Oct 2025 00:21:54 GMT  
		Size: 51.1 MB (51134403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b19bd1305d27429b498d99ea0d474fa352c9b5cef709cef8c65b435395b13b7`  
		Last Modified: Tue, 21 Oct 2025 01:55:49 GMT  
		Size: 10.6 MB (10554613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd6138bb1397bd153aa69988a6f6134130d90be20bd7a7be6703c803ab0ced`  
		Last Modified: Tue, 21 Oct 2025 01:55:46 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c582681fb9b847c3f33f65969de8cf3a71630dd1053c83f6115e5e267ade67`  
		Last Modified: Tue, 21 Oct 2025 01:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765e5b6fcd1395fadc4d12f363eaff394d524144b5e967c30c0123c91b27a2b2`  
		Last Modified: Tue, 21 Oct 2025 01:55:46 GMT  
		Size: 90.2 KB (90189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4979fc8fe1fe34bdcd595f92e0e11969da6f00b10c322515b1cf8cf8aa7d454`  
		Last Modified: Tue, 21 Oct 2025 01:55:46 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c4193ec4e622106dbf4b4d3401efe95b1b96aa129578eb4ddbe0d8ae2bc20d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de47aa3cdcb4062ad6aca20d0e9c45f54a00fc35a26ad7792af918aad68fedc7`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8f236a7714b52383e79c9f78576076d2136c94bbb407dbbf371ad4d327f6e`  
		Last Modified: Tue, 21 Oct 2025 10:08:34 GMT  
		Size: 3.6 MB (3601797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee92a53f5df2e13d1caaa40c75c0227124bb024d6c84faeae46edacd7bd7035`  
		Last Modified: Tue, 21 Oct 2025 10:08:35 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json
