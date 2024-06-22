## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:a7bc2e53e8f4616ee579759ea00bf7af1d5c0062ecc1638ea1b288f96f684bf3
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
$ docker pull neurodebian@sha256:cf480176ca4520ab1f5c8848ec95cd640b98db33b9fe6c0791ea06a5fdc550a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58591841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a114374404d5fb20bcd93318713c53bbaebd3209a68a16f081200914403bd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:23:33 GMT
ADD file:fb6f38952a56f7cbaa95d8ba94e80e8248829fe8e6ea398f1cbcb89942bd1547 in / 
# Thu, 13 Jun 2024 01:23:34 GMT
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
	-	`sha256:e1794c1f4707f1bb7231b64706e50d1615843d67660a3142771596a820e257b8`  
		Last Modified: Thu, 13 Jun 2024 01:29:39 GMT  
		Size: 52.3 MB (52277762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52909e6c675c108cf1cb17cf722cb11980f25b0920a3cc0f8633ab240f5b9b8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 6.2 MB (6222104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca531f42a81beec5bc990023652544af329efed80302dc0332d2eff4a45bc8f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87795856ca07eadb024a9d3008242192a8976da194829f60fc8edb55905708a9`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced51238b7394a553218045a8dca60b5e15cccc9429dfa0922dec76575e36c8c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 89.6 KB (89564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd23d654add65f4678ea40e8c8fd5a8eac55d626f61838b359ac57f9154686`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c2cdc7d4952fc763eb4befd9a9a11b53b792419de1611457240962f12312328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878ea552831c20aa15c8b82ea3ef9e26ba0fe77c54e5c3bf2537f6f810f93cdd`

```dockerfile
```

-	Layers:
	-	`sha256:ede7f304a946d86ed023d93a08cbc5205623f40cd1864005fa24f630cfef588d`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 3.6 MB (3551301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8545b04f670bc0a4881396967a718fa6bc676868eb1cf278b990ec1889ee641c`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f45065add2d0883b033a2583f09a8d0296d5b2745b1c2324e2c5a54ec3f82aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58826754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238b72f71b23c30823bcdb682d02953b3cc16a472ab5e249c0c188f6a4a9066c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
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
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf7f291b584d447470c53f740a381678ae64eb7277446eb7554834f38cd871e`  
		Last Modified: Fri, 21 Jun 2024 22:55:24 GMT  
		Size: 6.2 MB (6219741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ebd15e83f0eeb8343265465bc92b275299180a037a7280dddb86a897c405d`  
		Last Modified: Fri, 21 Jun 2024 22:55:24 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0cd3d386c4115201c955e348c507e250fe9f6c6a44c9d0ab6c06ea66413e79`  
		Last Modified: Fri, 21 Jun 2024 22:55:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ed7aec11adc4777ade35b4fd461be4e0547b4f74619300c17ffef4ef0e8f1c`  
		Last Modified: Fri, 21 Jun 2024 22:55:25 GMT  
		Size: 90.2 KB (90216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6f6f2bb716bdc9373cc55c9e5072c4e88376485cc431a7381ab13af841cdd`  
		Last Modified: Fri, 21 Jun 2024 22:55:45 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5fab77562e73a66d222647794863678beefd6a97c7d1f883b4ace2ce2f721db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bcd5c33752d5a7f98b2bb1a14a605deb310cf4298096a9619d7aee5915d69d`

```dockerfile
```

-	Layers:
	-	`sha256:4660fa1d0cf408df5c0a2d80f668921651c39ee94bca9f66ce46e5d783962f46`  
		Last Modified: Fri, 21 Jun 2024 22:55:45 GMT  
		Size: 3.6 MB (3552342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b1005c43c33d6249bc872230389aab9c470d30ad6ea4c21af84e773033063d`  
		Last Modified: Fri, 21 Jun 2024 22:55:45 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:66dab1622fbbe29b833cebc41b47710a8785d3856e6043f81a6a5b2b27fa731c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59791801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4804b743fa96675ac19b1ae1bcaf9dc7a9f4eae53f21d97411dfb4662642f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:32 GMT
ADD file:de9bc4e6489e3b2b2a8a1580ca8e391816a25c5cc50d80300c6624a24c656187 in / 
# Thu, 13 Jun 2024 00:41:33 GMT
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
	-	`sha256:c13178907b62803a756f9dd247be54c121b0e86bd70c25c38ec3ad97e2a3f6ed`  
		Last Modified: Thu, 13 Jun 2024 00:47:56 GMT  
		Size: 53.1 MB (53147470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710267daaaa3e6cdc9f432b35411c1d219ab924ed0018cbffd2e1caeb6849986`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 6.6 MB (6552408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d25a565d08def2085965e87bf8a652b6ed08e5ba43063c097a000edcb4834c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7febb4dd5c95e8995809c4868e23f968b23483d631af2127ebe274c54ebc7`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb6e6f8900e5cbfe958648e6b80077e7106738c347743d62f2b8803f694428`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 89.5 KB (89511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9037b079250aba9c446ed05fc6e1a348ba3464148e5dcbdae367153fdb5bd3a`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f02d25301f3c9cfaf51dc9563e275d77fe55b76ebd013cb7297a963cb992b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d86921de225cb5aa7773506438117f075c9660e9fd1bab44c642331ec9f3e`

```dockerfile
```

-	Layers:
	-	`sha256:0ff81c80afd7b93ec5b9a734f5cb7d1eae29b19ba9d75416e2db1bd8bdccace5`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.5 MB (3548399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a91eb0334fb2b49bf54cf7b4e6b6df2ebb36c86c489c72861e246ba13779ca`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json
