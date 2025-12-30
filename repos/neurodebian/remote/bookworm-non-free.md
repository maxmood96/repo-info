## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:1ae6cae90a44a169f9556fbd668691cc4acee59e1f35beae4f9a89a0025fd7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:abd11df33ce94245c5b308a02ac07a8a0db9d3ba22e30bf2ba86b8e53105a48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd504540067624ec06b2c5272b16151d76e122ffa720c3875f296e98a8ba9713`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:01:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9219b618e4e6182d17706ece800345bbb50e09f73c77956af27105335ff597f5`  
		Last Modified: Tue, 30 Dec 2025 00:01:25 GMT  
		Size: 11.3 MB (11269781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13e191d6357ce5e635c96f1043c54d607e416a6266aa6d684bed72db3a5f010`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6854b4553261e47e94358955f111b2475846ef1c8a4dab48857bb9f1a27e410`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da4d2477a14e4cb069f0a2140cc894b75cd66ad7b520df1deed197c3530388a`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ff8688eea57caa57840fef43d615760ba7ce668911891c755024d88ed3e7d8`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2cddb674f7050215234bc8be391bca98e2b8d08870fa1d3f4d46b017e1cb39c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec4de3b585e2c59818c179bff8a44609e5c58a301c70740835e9fc19e0714b`

```dockerfile
```

-	Layers:
	-	`sha256:7e55eee76bcffd1b4113daa63da2b2545d8f22a76ff8fabf8dfe0fcfbcf62e79`  
		Last Modified: Tue, 30 Dec 2025 02:08:14 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6521059055acdbe9eb6d741b62ff7e9c9d935dd808f3f6a5f29606ff245f7f43`  
		Last Modified: Tue, 30 Dec 2025 02:08:15 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:16b167b5084868ee4438b040d0e853f0983d1dbe370ecd6afc27b0cab1dd553e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544fa085ce3c72e8d91d7823155b0f299415f72adca3cf4159d4e6c780d05d8d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:01:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9572c2275cab572abb5887a4d4189ac1d16a900d802307d56f56d04e6ffc7dec`  
		Last Modified: Tue, 30 Dec 2025 00:01:39 GMT  
		Size: 11.3 MB (11253500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344bd7ca3dca19b442c7c96748dd10cee6b42422065e4b78e1c1e0d0c3eb1fc9`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70da94820edfa3b121d63698dbf16aa22dd1b90df6bf21411a9dee8ad9e8c199`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4555cee033ceaef40afc778e219498e0cbeaf00aa94df88e40ddf1ebc1ce47`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 93.5 KB (93530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62a2808c0e83420cf223b94befb2e48d1db29559e1a334c89e015733151897e`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8ca76a295a3584e1bba1a47d6224e58411fa0045cddfc42c11a2ed387162ff3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401e8b75ebeac47608271b90d088a56c0313183c4d4f84a5ca3293b0c2e19e49`

```dockerfile
```

-	Layers:
	-	`sha256:2aa7cfce6cff107c6e71a07fa4f85fc560fdfc5532c1e67d4016539deacdd99a`  
		Last Modified: Tue, 30 Dec 2025 02:08:20 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b0b3436e8d94f4f58c2bc0b789bbb969fae42b5437cbd6c8860d487d798f33`  
		Last Modified: Tue, 30 Dec 2025 02:08:21 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:54e39c0a7e601a013f26a89b43196c0f3271165e90ccd79569e2d50733db2ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6d2b960862fda49b19e40da9f2751adbbdaee0e0a868dfc49173abe55fe867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:49:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:49:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d27cc9ffb7903d292157edf3b1fb57175a2a59b66ae4855d328a6a97d9b4a6e9`  
		Last Modified: Mon, 29 Dec 2025 22:24:49 GMT  
		Size: 49.5 MB (49466879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82258aaaacbae7892b2268a26850ab0a1e85cd2a619b6712094fb04971123d48`  
		Last Modified: Mon, 29 Dec 2025 23:49:20 GMT  
		Size: 11.7 MB (11690184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a142d4d00e955924cd3766a4986bc364bd29309fffc7707bcf859f2af7317ee`  
		Last Modified: Mon, 29 Dec 2025 23:49:19 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3f75471d4d1de5965e43749ddcbe4142a7ae18ad68236518a90b5cf3931020`  
		Last Modified: Mon, 29 Dec 2025 23:49:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ac5274e2c5c25795e520bbc89b678809404ee3e65665c2fd3014375f38bb0b`  
		Last Modified: Mon, 29 Dec 2025 23:49:19 GMT  
		Size: 93.4 KB (93426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fe985b15805db21a9eb866bf442adb60ea238e0ad2673fc490a9416b6d050d`  
		Last Modified: Mon, 29 Dec 2025 23:49:19 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49f314e1dc4593a5b2b6be857c4eec25e5cf2d82a7bf0c516cd05fda7eb6fec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c836030afa4c39751f0bbddb7cf4467cd46df3fa62f9578119a9347e6fb9d5f`

```dockerfile
```

-	Layers:
	-	`sha256:4b997dff5fa03c308d34f21151ab1c5607afd395fd3a51458920e845a505f960`  
		Last Modified: Tue, 30 Dec 2025 05:07:52 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033f44be46e0bcc881e11e1543430fe7bb8849a8c5ae903e1ff356a2509f089f`  
		Last Modified: Tue, 30 Dec 2025 05:07:52 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
