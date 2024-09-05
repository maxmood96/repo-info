## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:fd8814700021a66ede779eefe13bf452b754ad98c0371a56dc3cee35f5543a44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:26a59f612ed56a4697f366a60a77194f5641af54e9a1664a020ed586da6d71f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59511253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f2ad76884e7f344ab5b0e055a2b96cca37774aef8be383075916292182c8af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2c007c64da352ec00a7c770959f382104c4122028f01d19283f85f7c5196e5`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 6.3 MB (6260869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e19ed26657edb9a90abf530ae502f28e31e1fcceca1c8faa0c42eca3a5984c`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d3b2c132c8026f38909d51e7a45f40fa7d65bfad4af42b8ff1cd3cae31b32`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5389944352d641fbf5d89602026b8119d8cf060cbdac213da804dbba99554b2`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 91.2 KB (91154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a05ede3e7172d449e69bd39da700fee287c4bfcf237b04a327d7c64236ff83e`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc86531131eff71b8b0308bd0c49133fb6956878d87c78527fb4d8c92332daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c70794af3101644cfd9922da9e9cf1d6e31f20c36f21ce04b23f581344a9ef`

```dockerfile
```

-	Layers:
	-	`sha256:2dfae5164f018ebc1798d623dbc99edff836f35311794491eaf4a62521db0c5b`  
		Last Modified: Wed, 04 Sep 2024 23:11:00 GMT  
		Size: 3.5 MB (3532496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155d36edcf9182b5d9cd047985eadbb745b640d0e8d69fb82d6ffba6986d16e1`  
		Last Modified: Wed, 04 Sep 2024 23:10:59 GMT  
		Size: 15.4 KB (15428 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:61b1335fe95c43cbba5331e564ed344d9a1117fadb9f2d8b7e9cda08ef005df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb4b41d27fe8f8f38614f5f9d18334ac64546deb807d9c24f9a8bc2e7d6994`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408855a53c5bbe2210b3acb92872348f336eed207c1fd565aa9a1894ae3360d7`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 6.2 MB (6248358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513957bcba9f74ca0a80d4f0d2a013c85dedaca9c3d7851562387b57f917f6d2`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b06fa225e64f5f4e0e613985a5fad9decc48bec4c0f6976a7c73a3096c5526`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda73a6bab6cbe0f0ae9577ec42d105d5e08ef05319ea5926169e01c3432901`  
		Last Modified: Thu, 05 Sep 2024 12:38:02 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516d23c8c2424b41423a5203bfe7ee2dc27bf78f1d423bfaec155350b83b067`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5abfd6e5ca6a2a3a60e3fc06b0a35c972fd31f3d60e35f3768dad4b3d718edaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b783683a14f28eebc05c5436416cd4da84c4587b6c3d69deb4e3b1e9e7997a`

```dockerfile
```

-	Layers:
	-	`sha256:cb59bdc05b436dafa348c7fe82a7d452321c84d9ae796567c4450919ca49b515`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 3.5 MB (3533538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94fe3d7fc11ba1ba4aaafdb2d86aa83d27096203ad2c8924782d0df67b3d4a1`  
		Last Modified: Thu, 05 Sep 2024 12:38:22 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f262c8cff769b5b5310497956549cf54f5d9d71cfe7fa65799b481b869d6df13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60713808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a1dc652e1a803d21c1f7e3dfde6b5a2af5e9cebc49a802db06584b02ef4a7e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f53d49502772dd0bb2f4018a9034a0e325b9bd5f66244b738ad7515867ff34`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 6.6 MB (6587150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c740fedab1abb15223181bef8f90748bae271cea4d437f5c2f518598dae6edd7`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823374c8ade17fe49d3c94df03cddf3b957757051a48a68d056d91a1fbdc2091`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f993073d6e21d91c9082e35660a4a9afadf1ac920c59c5f3cf4c25232ba916`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 91.0 KB (91016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09943a1a6a592c8712c972bc5a4b91341501f19f6b14f36af6e8cf7dcda3ea2`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b1af0d66201c66bc02711ccfd849087130f60b5998ef91f7400a0607bbfa1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbecb14dbfbba53dea46422867f787375bcbe260c646f86cbc50b8da14a7827`

```dockerfile
```

-	Layers:
	-	`sha256:c6b7d3f4ce778effc987750d2dfd188f3f768d3db1b6ac2ccc8b8dcb95ce6af0`  
		Last Modified: Thu, 05 Sep 2024 00:15:29 GMT  
		Size: 3.5 MB (3529595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bdcc3c9e286ab8883d59427bf8adfe9dc5aff9df257183bc8edfcdfa01a37a`  
		Last Modified: Thu, 05 Sep 2024 00:15:28 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json
