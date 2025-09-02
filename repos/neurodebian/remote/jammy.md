## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:4680ce4f3aa96ba81cd6fa10632a951db3fd0bff6cecaa8bf2b4f733bf696a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3ce910a25e1ada8fb29113c427d363d0950df18f993942bb1e966b293c906fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc492e3e53cf64bb4f5f322e8772c61cb99e0627ce806d72563b7cd165fa6c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a4724a87526948a669d180182a6778e1e691c719838765abce4d01c46d3989`  
		Last Modified: Tue, 02 Sep 2025 00:23:48 GMT  
		Size: 3.6 MB (3625618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c380e33d94fb72232b49c8bc34ed7ec6d5fc476094360c374549509f46be63`  
		Last Modified: Tue, 02 Sep 2025 00:23:47 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5b8f40e27413a9ed04a139b53a2d27ad574119fb38e07573119b5f1ba2b7cb`  
		Last Modified: Tue, 02 Sep 2025 00:23:41 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f236e29b2af85abd6976a93143c874089cd671b6c9dce78ea9370ae33bedea`  
		Last Modified: Tue, 02 Sep 2025 00:23:42 GMT  
		Size: 110.6 KB (110589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:34aff235caca5114ffe5988df3758c029134f3cfd79928f2b7b75e046d884177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35a861e1f8209aec3893a6055acb4e242ebe33c2703d85a893b48ff3b02363a`

```dockerfile
```

-	Layers:
	-	`sha256:7d41caedea004a5f24a35b74306fc2bb1a9a276bf38f155d55be744db8ac4a1e`  
		Last Modified: Tue, 02 Sep 2025 01:07:20 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09e2e050c9cb1cb84b85074083ff037333a48e8c7fdc30b0f24b2e72482d686`  
		Last Modified: Tue, 02 Sep 2025 01:07:21 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad8b5021080af09840051d598a139cc1c51c5efd96106321e1c90e24d044331b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffecd0a6844d208ea0f4506ccde69a244b06ffa5e778636e6460a540b30e23fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c79060279f7aa5b518a13677c95296260b1886a9f06c0e227470f215e83ade0`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 3.6 MB (3598083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b131986ef9be15153a34c64bfff28f038121b1c7c30140d9bd1989ac1bc8e1b`  
		Last Modified: Tue, 12 Aug 2025 20:32:53 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172ce265d02bd87f8e4121afa9fcae149080ac766bda336aed21bb4709d2c93a`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffdd963c92937ca675977e8fc095b7dc1053938bd089842f31e5a5b575a3445`  
		Last Modified: Tue, 12 Aug 2025 20:32:54 GMT  
		Size: 110.5 KB (110546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a5e7e4f3b165d34fb2b0551c78a2ff2ac49e39100f1fdc4ec8ea55cbb11a4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e172ac10e0efc41d919cdddd439714cc3a31ce8e2402d91a16378065109184ca`

```dockerfile
```

-	Layers:
	-	`sha256:845a10a1ee83d7027ba8904d7ae03bb1741ff736c904e2aa0a744f5a41812511`  
		Last Modified: Tue, 12 Aug 2025 22:07:25 GMT  
		Size: 2.2 MB (2198564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017a69c5cc0e714fad05106e616c4c380eda5a105290ccc493961416fc91c597`  
		Last Modified: Tue, 12 Aug 2025 22:07:26 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json
