## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:4a017e0df81ee8217f5c57edff44c5ab6f90a60a99f40854c81f6a6f11c60384
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
$ docker pull neurodebian@sha256:de9deb09a9c4a574733d8bf0ee9a8435ca602569681432e0e590c0293bd56639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59972303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd450a6e5b8e10e76c6e84376a6dabc34200b6d18baa5cf78ed1fe5c5eb2ea4b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
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
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcc1f5af84d08060d7baeab3587692d4e1469721eaf97086e62e8a08e46bffe`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c889b01f93a511698d8f75dec67873b2853e860e6b4fe77a705985d114ee6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75670270a37805095bebb659f19bb51c4a240cc626b2d8de23d774dac2059c63`

```dockerfile
```

-	Layers:
	-	`sha256:3d01e9874db9175f10aac3e72aa9bbdb68bc9c22142cafda74af046e7cc9999b`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 3.5 MB (3543935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11aab390c169d17bca4c29d127707bcd1072e69e4adf4beabeea95ad9335d9b6`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 15.8 KB (15755 bytes)  
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
