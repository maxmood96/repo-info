## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:8aa073c3cd5fbed8f89f21e0cfc35a9d4a6fb7c1c1b16c96c1185a11b156b74f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a30d0910eee54e78cff1ebacfbf94d0f5d1bcfb233729937a5383b3b8754aebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59860224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58b7b67a10ad31319482f49ce07ffaed1409f4bdc42bdb57591f94a9f55f870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463f8d68a16e9ac92c12f43868402c6f3f57d26fdad10a18f8469cbe505b5557`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 6.5 MB (6527838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb52b6a48245f5a8831658b3aabe3cf7c7ff05fac76e80b3f6301fae8148095c`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d374d800c72b49ed8fe36ec4a126f57a5db7d2354dd3a32c800f1143d1a7`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0266e43d73ad49f9d716b54f8d979e37b5114c365d04ef4a24186995d7ec2739`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 91.2 KB (91229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf7b9db2b69c3f521edd6792979833642d688b878bb51d6390bb1461a1fa26d`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bcdc6c21779357df565f1ad14a6f8c8508b2a8dc04d4b1dbbc25d4b2cd773cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575d2ce06e3134c6340d5878b4d0403f24d2d7ebc47116f54490e5c6a19ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:26e7003cef78c34f6c8b2ab579f8ffd7624e7c5566f72feec2ab5465909c0ad7`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 3.5 MB (3538040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51fb57aa93986c771ed7fb9e961105a680c9f6cd0999e682188320cdf94ee724`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9800c97a370a781ffb9871de33494c3a06907666e74ec5dfd30006c9acd5d149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49241192e3ffb655678dd748976796c720d47028f0001ebb417840254c4d9524`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507ba0d1af87c79eb5ed21e470daeb6651cd6fd35ac71c7f4316437bcf9838b`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 6.5 MB (6513412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea37e5d08e4432023f6c69cebd438dd20a209a3cd3b94eb789a8c4f80f5fb74`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7766e08b26d04d33fce1a14d04e2233cb4eb74cda5d72aaa29f51748001414e`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41352cbfcbfbb365bc31271939a7c8835966e68a87266f29c649ba4302e4f95`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 91.9 KB (91941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45f485faecfdb395798bd27324e61884a7fa42eb02cb31494f7362503104`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4bf8e13d9e5fde0aa2ec003ed93ba575b296b6a1fa393a343426333a5f3bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67a8e580c3f4979cbb59915aab3ad2437957ad387641a293eb5a716dab2d9b`

```dockerfile
```

-	Layers:
	-	`sha256:2a1b5b9e67e1dc1eb6abb7fe584c62fd8dc2ddf3e9842df732676c693cc1a80d`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 3.5 MB (3539082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b9375ffc08954ec2b358f015f7142cdbd3b31bc5835e0cbea70ffa77c06bad`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 15.6 KB (15649 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9c7f1e28a81eaa0320511416c4df234ad4f7600f45586e56abaf446d54c8c688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61046012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441a3e6af0dfa8112ae47502d4c44271690c8d39f51606037000ff9ad08129cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1ffc8190a07ef94376d2867dd7a73d310a6dd7481cc9c26c1a309cefcc3be5`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 6.9 MB (6874953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00ac0906fe55639580577bbd3dd60b722d4c59033a0c14446e5224830a05c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dbbc38a72670aac92fe8264b45b65f1639ceab86ba73989947c33f06386fc4`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cabfbcdfe93633e99167f3116691d7916d684a7d81ea43d9a4b36b13fa770b`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 91.2 KB (91188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3116d94f84b7b8a0808de899de4b7a8d7c6b78353d6d93203f567f84b724d03c`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a6b2876e6dad21b09173111ef3753a8715147a7e56ae7770dc4060809e034a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617bea8eecaa56f0a9d3b22db9198bfe101fe2ac785cb3c5575ee8ea44214b3f`

```dockerfile
```

-	Layers:
	-	`sha256:b89f9486666bcd9109be18c9320b58d7dfcc763af91aa24e924946324820d2b2`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.5 MB (3535137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed201cf8df404b1835b3c3e3e5206232c9e3cb0be2bdf87e8ee937c6c6b19e04`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 15.5 KB (15488 bytes)  
		MIME: application/vnd.in-toto+json
