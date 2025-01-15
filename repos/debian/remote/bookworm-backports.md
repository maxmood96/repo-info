## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:8a4530de06907c29045b43536500fe02f6be00fe110d907b7751305936a22c3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:2f28e9c71b5d6fa61cfc817faac1531bb646ebc78d5b99c456eeff82ae9f381d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e02e3c5f44500b59fab75a106287b2f0e2040b654213df2faf11cd1c04118b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de5c44f675ef6713fdfc570e421fdc78a41890d54671e33073ecf4b4e2d62da`  
		Last Modified: Tue, 14 Jan 2025 02:15:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9812fddd933cf2b14b03a486a51959c5051c919c285d03e2530856f9fde7fee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbeeba70307dbdca0ef8840890c931a618d46701be6fec57d441b108a4104dc`

```dockerfile
```

-	Layers:
	-	`sha256:b73480e63deab12683b8d7dd093411538ba36a21fd70425f1e243b58bdec9e68`  
		Last Modified: Tue, 14 Jan 2025 02:15:55 GMT  
		Size: 3.6 MB (3619210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5792d548a07770c7d9da6bb0e3e2fe155961c4ca1e5af4014faf997af9dc2ca3`  
		Last Modified: Tue, 14 Jan 2025 02:15:55 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2d00c9319458f7042a4948626da2f8ad802df9690e281b1f25dbd381a102269b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46007039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055a4367223b4f311e97e57994441d150c147c2eddfce1a4d1ac80a0892255a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:237814a70d9f7e95f3568236c75036fcef22a88f1a76245129eca111484c0351`  
		Last Modified: Tue, 14 Jan 2025 01:33:00 GMT  
		Size: 46.0 MB (46006814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b108a18cda19d59d9ea45a8b320ebedaf474a3e3f2cb2d725fcc0b42427ff82`  
		Last Modified: Tue, 14 Jan 2025 02:15:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:23eeecffa5568007d3fc435b16e23a9d82370695d7e324372535a233a9efc4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79a422018680405892be674c513fffce555f91d92afbb91a621643830843df`

```dockerfile
```

-	Layers:
	-	`sha256:d384855435a2978e502041af2b92bf11e8f59a2ca0f8ef1016b49e3db6e77dff`  
		Last Modified: Tue, 14 Jan 2025 02:15:57 GMT  
		Size: 3.6 MB (3619411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090b1a041eba72f86b966b2d656c56dc6dad4594bb92a6a4c7cce422ccf915ca`  
		Last Modified: Tue, 14 Jan 2025 02:15:57 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bba2eab4320233e80b393c75c2c8e6fcffbd9715a40609f6624b4d85d68582a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44184433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe3b568aefdfff4137b2f0cf17c7b8074936ed04c74986b8b7aeb6cc039b06f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff97800c545e1461c27e0b6cab0d0647279def6385dbb2825ae260035b18cbb`  
		Last Modified: Tue, 14 Jan 2025 02:17:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7090668cf50711c4388c010f9e7fe49d45f8741106acbf46a7a3a7c87c3db9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1229fdc3697fd7c9464570c2289dca1f0b4a8fdd0906c21b7728143c7a33d9d0`

```dockerfile
```

-	Layers:
	-	`sha256:82e79f02f72a1aba516a8ad6814e3110bc5765183701160251c466ee6bdc8696`  
		Last Modified: Tue, 14 Jan 2025 02:17:07 GMT  
		Size: 3.6 MB (3621389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5bb02f682772e1738e332f93ff6238bd92d055ed64da28f1778bdd0064f077`  
		Last Modified: Tue, 14 Jan 2025 02:17:06 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9987b6c8fda950bd88d140fb862a8a77304f653ec50ceca1b70de85ecf1d055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48307120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8a0e970c02ba58c909d166cc1113f9b946ce1654ecba38916602c380de280b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ce5606027917ba62d80408a9623266f2c92de76f69307cb8b3db66688faa83`  
		Last Modified: Tue, 14 Jan 2025 03:03:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5c006d6dfd90b61421dfc0a516d7496932f0eea8c1c2a8c7a3e1575516f57463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7c505a1a784c18bf4ea81eb9959d957a51e37270cae5db8846867c4376c2ef`

```dockerfile
```

-	Layers:
	-	`sha256:711da86de761d30d74b8b69a90cb573fb5610d1edd3435e7deefd69b5fad94af`  
		Last Modified: Tue, 14 Jan 2025 03:03:31 GMT  
		Size: 3.6 MB (3619425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68d587c486fc90681870333c7dabc0c721458a22563d4ab68c5165fef95e810`  
		Last Modified: Tue, 14 Jan 2025 03:03:31 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:0ccab6d910cc9a5b65f3b981de367c24b3986761f86be17470fed12200e304cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49457970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1b401e9fa63cfffa8321e3d1747fd778c061a4ee8c7d11d2278e49887c1b43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 20:42:04 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0bfb5773dcc119b91c8f34f0e65c18c678b3069a596059698aa42785d42ab9`  
		Last Modified: Tue, 14 Jan 2025 02:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:119b15f5bb2fc9a246a493c022d6d052899c41917e63917aef0ea1490cfb4a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d05e37043b933ab9631061beb369f7a6cf7b3b9c3800102f8238e9136ef854`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d68c9f3de08e94d7376510fbefa96e3c588afc751fcdc8bece83e3631382c`  
		Last Modified: Tue, 14 Jan 2025 02:15:40 GMT  
		Size: 3.6 MB (3616371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eaab5fad8439543a163305fb852df72ba29b5cb133092f4184723046c53c62`  
		Last Modified: Tue, 14 Jan 2025 02:15:40 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ee2309987e4786b564236bd8df9b9f78bcf2037564c4322deef6eb16f3e4369b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48758325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9e8c9576e3d25783637c9462f068ad060ed45557f7f0869722786b9a090f64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 20:45:22 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372c6f07f712c98c75bf738273b1b91214ba9bb511138f2940b3a63959588128`  
		Last Modified: Tue, 14 Jan 2025 02:17:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e13d8824a6b73946e8c0e4059a38502e534f4e59be2997c458255e54767791a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f65243e059d16694a2ae2eaf4fece46ac522e6c5be2f6c7b558040eeb31f01`

```dockerfile
```

-	Layers:
	-	`sha256:7acf7035aa333c557fff51ccef74a01f3254d5d924e2aceeaaf59bab2a7d67ee`  
		Last Modified: Tue, 14 Jan 2025 02:17:00 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ca97a2f27fcf356544a5eb8c5729d8fb07a504fa6cac945d0c3a40e84eb1c3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52313361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d124e7b2caeef6162fbd33c73283e5092ab1532ea10198ef3d6f03c829ab652e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 20:37:16 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c1b65feed107d300b53d2e60994fe6df4d4c1af1fa9b9a6a9953e564ac670f`  
		Last Modified: Tue, 14 Jan 2025 02:38:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:97f697df8857cf02a0f95dd06164b408d1701c5c1f5fc84df6793da2bab1e0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258952b89e8ec698f81a0483be104bf6662d1b55b3b38a757ded82f23cd9c990`

```dockerfile
```

-	Layers:
	-	`sha256:eafeb318d870eb13e0f47eb20bddb2c1ed09548b8f3e96fd1bd6ea5caef50278`  
		Last Modified: Tue, 14 Jan 2025 02:38:01 GMT  
		Size: 3.6 MB (3623470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59aa2f5f22391e8d37357842baee0e712bec5d1b434edea4b6e20cab9c05d1a3`  
		Last Modified: Tue, 14 Jan 2025 02:38:00 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:760b42d4bdffced8c1087d71446f3e5738481d5de06fad966d2743b781d6088c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47132005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6238edab8cbd04cd14f64741e0f66edcc5bdf24379df16fff2ff05a0adccfc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Mon, 13 Jan 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 20:37:18 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e5206e779621cdfebe18bfa2692f264bad105996356c9f2ac231e8186c2345`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:79285f18c0755071250f5926cd2491c2269949ef3f26a16f048830f85d40d942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242104a5ffb2354035b7828174ed7c9a4bf8e11100d53832f030262989e4def2`

```dockerfile
```

-	Layers:
	-	`sha256:0c1d71a8789f2cbdf18d01ae563bf3a928fcbd41c139f02d45639c2609f7386d`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 3.6 MB (3618940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa3b8176cbf2ef46d2acdd18c14217f2a5ba835aabd143edb3730860c5219e8`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
