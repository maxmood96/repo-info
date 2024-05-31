## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:0ea6a040d3005bbc6d6adbde1b3c4dae2d89a4c4dd943ba32aa350e14452886f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:18169413818de1fdc43e158c849d34850b02a6390905f424f8b10ca50211ea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30487499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad09230fe8daacf1f1a34dc9035a37fbae4351949aa366e5f398789759a0b839`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e5846e93887a546e4f0410696260f4c77e386470678fb9087874d2e2524648`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 4.7 MB (4687092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed4ee21cce42c14e3fb8fc307e972c22e1f37766ce10ea56c1b9a8a0a3b4e7f`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9dc044f0c27fa2a4801bd9cfe358b5963621bb4678ed04eaeaa39b47e216d`  
		Last Modified: Fri, 31 May 2024 01:53:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc8e83d4f824da3b76b601e84201c6a07c69a82d7fccea5c2c38a089959d580`  
		Last Modified: Fri, 31 May 2024 01:53:28 GMT  
		Size: 107.0 KB (106976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8aac03308dee46930f831ecbedcb6dbbfff06484b3e1e610839f45e1bc49e9`  
		Last Modified: Fri, 31 May 2024 01:53:28 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bionic-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:880afd29b8e91716e066711fb12dc7f417be006872cbaccd832e847019ef7cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1923112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f4199010c3c203b7b6090e2041c2d2d807bba800667a37d79712217f5d9782`

```dockerfile
```

-	Layers:
	-	`sha256:9ca82aa12724fbd0393e316e569d6ce7b654947400243964ec2d7559dd11f17b`  
		Last Modified: Fri, 31 May 2024 01:53:27 GMT  
		Size: 1.9 MB (1907511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd1a8a30123b9a8b1f54a4c61dcc0b6bd5ff9ebfaf54e0d66be9e3d7b9a925a`  
		Last Modified: Fri, 31 May 2024 01:53:26 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c0087fb2593667a29da5e15ca6c6195d981098e591806dbc153c933ab206780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27091244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854f697b18ee9a7e7576402c46570e83539fea823644d026b982df4cad449eba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda72376ca07b81a58afcd07ab707bd2b65eaaf4b638adda578079eff8f5024`  
		Last Modified: Fri, 31 May 2024 11:26:02 GMT  
		Size: 4.3 MB (4268722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386017dd0da8e1005b1406e7a864fd7c7378741bac7f1e6974da156b71c24f3`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d876a1c7682fb795ebc1e91e721061bfbdcea91113e6cf1289eddeb3ab5774`  
		Last Modified: Fri, 31 May 2024 11:26:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b133983b820f58b53a8477086ebb696d7ca345e5daf8210097cde1b3d6f130c9`  
		Last Modified: Fri, 31 May 2024 11:26:03 GMT  
		Size: 106.9 KB (106852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3db3528f80fffc9adc3f1840a8ce5597384283543a1634e3a255e81a5affd8`  
		Last Modified: Fri, 31 May 2024 12:13:46 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bionic-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a98b30791125fe37b5ddf48f5d03eddced0fda6fb5f219e49c18dff3963021e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1923573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd87183851da7fa8aa438d607d5c9dd841e3703014a8d9bb101d01f972e7c472`

```dockerfile
```

-	Layers:
	-	`sha256:6bd54ab750554eea7ef069ed465d824a8167370a301986aa94720c173807a075`  
		Last Modified: Fri, 31 May 2024 12:13:46 GMT  
		Size: 1.9 MB (1907694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1028c37d9672e46133b86c2713ededb3f570948468eac19912954a30057615`  
		Last Modified: Fri, 31 May 2024 12:13:45 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
