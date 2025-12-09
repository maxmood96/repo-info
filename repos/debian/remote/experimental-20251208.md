## `debian:experimental-20251208`

```console
$ docker pull debian@sha256:7621ca4301c71ba2d4d2657ae1d6737924df3016cff90af57142c365287ec597
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `debian:experimental-20251208` - linux; amd64

```console
$ docker pull debian@sha256:eb13760ecf2111f560a6bc4970aeae20b0beb1a8a9b3b31faf420903e9bb7bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48817754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db64da441e0bd0df1458476060c55dd0ec783903eaf8d8d4e457317abe4d5970`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1765152000'
# Mon, 08 Dec 2025 22:32:52 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8d9b0d1957d2d6b829931b44287ff6fbd7c33842026a1775ba2e0472c68a9d6e`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 48.8 MB (48817530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e37c1128318757608dcc276f033ab9fe3d6519e74c47ae37e315928b2ec2036`  
		Last Modified: Mon, 08 Dec 2025 22:33:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251208` - unknown; unknown

```console
$ docker pull debian@sha256:77df7597a1e7a9cc6a8639a2a9b0a11d78f965895a09c766a5083a5bf74ab4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c6bd492a5d2950366a5f42a41b7124a62d45985fbde4d6bd3567d26849af3b`

```dockerfile
```

-	Layers:
	-	`sha256:9af002aef2c1e5a72e6966d8950fa09c38585820cac7e1994b55298d44a3594a`  
		Last Modified: Tue, 09 Dec 2025 01:26:15 GMT  
		Size: 3.1 MB (3139612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926e6694c48dcf3303bad3f3b29946326dd8c7aa9807cc0086d6915b40d2cf44`  
		Last Modified: Tue, 09 Dec 2025 01:26:16 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251208` - linux; arm variant v7

```console
$ docker pull debian@sha256:f394ac1f5ed28a76061263042bbd8e7dbbdff22c02da280ffe5dd0c1219d1af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45118604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43349534d4fbd27597622d74053fa23f1c2d7a70bd424a68c1f9cffeed69cb91`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1765152000'
# Mon, 08 Dec 2025 22:32:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:489898ba097c6a4674171295263c2673a8d0769663194b84ac7501f0ac913233`  
		Last Modified: Mon, 08 Dec 2025 22:16:43 GMT  
		Size: 45.1 MB (45118383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecf59b035097ac1309343d4e54d24d95941213a75955f1b8f4f8840a729be14`  
		Last Modified: Mon, 08 Dec 2025 22:32:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251208` - unknown; unknown

```console
$ docker pull debian@sha256:856dca3ae3e385480b24718d2850cdd7f4d57de934b4939c2bad1d49f650dd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29864930c4de17398acb716048ab1e7821b1da30e5f8b2254c547d330f444c17`

```dockerfile
```

-	Layers:
	-	`sha256:7c8984a4290829d2d01d9aa2331edc4ea9dcb62000a4b1cd5b40b632d8877326`  
		Last Modified: Tue, 09 Dec 2025 01:26:24 GMT  
		Size: 3.1 MB (3140988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42cb5a16600a549899f293997afe270e15665b8d9d00b44a472c1ca2751a767`  
		Last Modified: Tue, 09 Dec 2025 01:26:25 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251208` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:69adbf4e38ca686e2c0d8d86e324fe76ec762f34af8e2412a82a252f0949bd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48838834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10702629e8906afe5a96246acb940bcc4c18846a0d6c78eaf93fecbb2d6e2e15`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1765152000'
# Mon, 08 Dec 2025 22:31:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f162a7a61e3a94d76528bcd3e31cf4caa498b91c942b372834ed6045eb210caf`  
		Last Modified: Mon, 08 Dec 2025 22:17:44 GMT  
		Size: 48.8 MB (48838614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f948fee4142eb938ea805a02f80ac41f6889ad9cc4cd491820bebda7407163`  
		Last Modified: Mon, 08 Dec 2025 22:32:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251208` - unknown; unknown

```console
$ docker pull debian@sha256:5d27ed0a2af3984ee75b5bfc91789cfe6582b7c3c9a39ce5c94abdecfb7fda33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fded121f850bfb1fe0d16698a9560174d7fc8e9fdb41e948ed81c2647ce0910f`

```dockerfile
```

-	Layers:
	-	`sha256:ce28187af451b8eb8cc23b93a2aecc8495253c876caf9b84ad625ba789d7225c`  
		Last Modified: Tue, 09 Dec 2025 01:26:30 GMT  
		Size: 3.1 MB (3140465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b140d52f47c3a95f68e6378f16a37e1a61a7722c342e960f054962232e3f34`  
		Last Modified: Tue, 09 Dec 2025 01:26:30 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251208` - linux; 386

```console
$ docker pull debian@sha256:0996cbd00a136c916751971ed77852129996a0b55185c1905cebb34f25164424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49948193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c48d03a3cc38ac3ceb2261cd3af21250fa81c84e662f89b5208d07ee53e4ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1765152000'
# Mon, 08 Dec 2025 22:31:53 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:847f716ac68160daecc57bf4272dafe63b088b152337db6b749737bd78f59163`  
		Last Modified: Mon, 08 Dec 2025 22:17:34 GMT  
		Size: 49.9 MB (49947973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98822a4ea8b17fdc62dfa1e5a94baefd066bcfa3fd63c90eb7433fc53809c005`  
		Last Modified: Mon, 08 Dec 2025 22:32:06 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251208` - unknown; unknown

```console
$ docker pull debian@sha256:38dea26c4d17ee8a64281e2f6a9baaeb452e19d3b48bd51cad997cfd94a3e627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf9124d8c06a6c551fe43cfccdabef2460b04bc84bf45ddec073f79fe0105e6`

```dockerfile
```

-	Layers:
	-	`sha256:4e9179eb0901ee4e04757f32ceac108f628328a6e20b6692ec76e0a4d12e1ae1`  
		Last Modified: Tue, 09 Dec 2025 01:26:34 GMT  
		Size: 3.1 MB (3136812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:957924927f9bd838a7b14c6296c185222ea3e8acd1b1e555d2f334ec2d8060e6`  
		Last Modified: Tue, 09 Dec 2025 01:26:35 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251208` - linux; ppc64le

```console
$ docker pull debian@sha256:1cc727fa4a0d8a3c842efd25c547f4a116d86cc58429864c1a3529ee2b0bba20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53494655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469523a2dde5c2deb094978596832bc58778a3e0aca1eabf9160d29487e9f137`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1765152000'
# Mon, 08 Dec 2025 23:20:06 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bd678e1868ddc1c12a3b9ccb73f86c32a2395d3368d7e2716366aede4a924be9`  
		Last Modified: Mon, 08 Dec 2025 22:53:07 GMT  
		Size: 53.5 MB (53494431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c52a6e434a588885aa1bdf11c3aeda7a538e1088bd7bd529987dee17c77a1`  
		Last Modified: Mon, 08 Dec 2025 23:20:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251208` - unknown; unknown

```console
$ docker pull debian@sha256:5d095c20b2b76a675351de954fac1b6d93f36f01903c0c861cc9947b1b7d5321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46be1bcd13344abd81a89af354468cfa49e165b976c39000eefaa7cfc0afda0a`

```dockerfile
```

-	Layers:
	-	`sha256:a460619183f51a5b280cc355419fc9f21628f4ed12ec3d661b8b2ad09e07aa67`  
		Last Modified: Tue, 09 Dec 2025 01:26:40 GMT  
		Size: 3.1 MB (3143119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96ace99a8fff238f178f7a9361b7cbd97bc80281b2dbd819afb4a0930826092`  
		Last Modified: Tue, 09 Dec 2025 01:26:41 GMT  
		Size: 6.1 KB (6132 bytes)  
		MIME: application/vnd.in-toto+json
