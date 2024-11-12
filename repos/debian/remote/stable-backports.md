## `debian:stable-backports`

```console
$ docker pull debian@sha256:9e4e2c790da6f5f8fdc166e758a9d499786a5196ebcb33451f840d645102d7ad
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:8f97d0a4dc7ace3da025e3398a5e34701ff19833169d8c82a6e845da9850f368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49575900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce973053ebb2600b866fd005935db027d1e6f7f9f7ed914638c14007007b26b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6c35a25294ffd03da9b57aac6171f6994cef78277302cb071bde7459d133d299`  
		Last Modified: Tue, 12 Nov 2024 00:55:12 GMT  
		Size: 49.6 MB (49575679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca0a24abdb91f6a0758d98433b4599d3d4fdcd424592924a467c6597e686c4e`  
		Last Modified: Tue, 12 Nov 2024 02:01:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d96730e9636817565b8c6f57b967ed172ded43a1f5a38c6f8bd66d8df98fd6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241a5f7d025de35fb74b821fe9aeb01c6a60a4a12b3c8eba265cbbaaf2ad4c4c`

```dockerfile
```

-	Layers:
	-	`sha256:c56b4582010c4a87a041870c63313f7277785f806c67adcebcfeface728a1f37`  
		Last Modified: Tue, 12 Nov 2024 02:01:51 GMT  
		Size: 3.6 MB (3624278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ebc1b75a28ec77d820ca33e732fca6290a2a20e5f07c32f45261b8072970d55`  
		Last Modified: Tue, 12 Nov 2024 02:01:50 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4dfca14b023d8734ae5328fdfb8c341425bb3d9a444b3c7a11ae397453b69140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47339022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff458735deefd5af7354de7d6fd20cb478de9ea68d3e7ec6248aa88d822735ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7fc34a983ec56730b28646f4cc17636d9b156fd84d06af5368cae358ca5f5698`  
		Last Modified: Tue, 12 Nov 2024 00:56:49 GMT  
		Size: 47.3 MB (47338800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580bf25b2e8cc0ab3c0668b96aa95267d59c3e76ec0581ef4d64790a327f51dc`  
		Last Modified: Tue, 12 Nov 2024 02:01:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2ac678de41f13e7cef4e2832efef8c8bc41924e211a1b858987cbe851a003c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac803ce770f04d9d7702139717e650431b779c7d92b3d24e62644e6c994490e`

```dockerfile
```

-	Layers:
	-	`sha256:ba59d5795696531014ad942e200c63451456ac828609ea936f1bbb997a3cb88e`  
		Last Modified: Tue, 12 Nov 2024 02:01:39 GMT  
		Size: 3.6 MB (3624478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb2e3c6f6b2d868fb19d4ad172052380b084eb6b4647824382fe61426694e5e`  
		Last Modified: Tue, 12 Nov 2024 02:01:38 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:732a8a2280b2b2dabf17130dac49273bab021baa30cc3df338d2f63a30c76e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45150755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880917b121752f20d50a9a954fa547f228190d436b514d1dfa28e0452ff97984`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b3816494cadb7bbebc8d0b3144d1bed175d21f44699328d1ec2964eef279693a`  
		Last Modified: Tue, 12 Nov 2024 01:00:42 GMT  
		Size: 45.2 MB (45150532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2079de95c5f3b858da15a82e23447ec5dc64b64fcf664cc8e2ac96240d0b844c`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b520f3a35df66c84e2d42c8741e9586f50e4e7569fce37874add0f97965d1176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54e599a2c318ff595be91d63a99c37e954553467423b00a3e2ae5b8ccbcf493`

```dockerfile
```

-	Layers:
	-	`sha256:8df7fcc3f50c8c81297bcf1885f611b3daf51b6728f313b5cbd0485f7ba822a9`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 3.6 MB (3626456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0daca2e5a341a172faff523b7b4b6b070405d20bbfd7fc544b83f98198e7fd6`  
		Last Modified: Tue, 12 Nov 2024 02:21:06 GMT  
		Size: 5.9 KB (5877 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:75a1fe04e05025d59c7833d2057ed46dffb0bd023b410b3961a6e0ffb0bba406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49587428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91ae269bbec7ad26027fd5340ac17b1c6be58a2454e8d410fb58ac776341bd1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2d0f3265ee43f0ebd0a392d8645eb687f2f1cb6ea4079e325357fe61a8a38856`  
		Last Modified: Tue, 12 Nov 2024 01:00:55 GMT  
		Size: 49.6 MB (49587205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fa6f05449968c24cd8398f6360f7540d1a42205ae8372f84b665d97e53c508`  
		Last Modified: Tue, 12 Nov 2024 02:23:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2ffbaba62d78514ba14dcb4e79d4dbd892669ad3d6057b60e8f947a8a011dbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17ef670ac74fb2a895bb7878d96a6a2a025ed48a52c359695c04f3c784b9651`

```dockerfile
```

-	Layers:
	-	`sha256:8e22a6dd81b68ef46a12528ee31a0ee5b14387bed0fde207e2db9547574d7cf7`  
		Last Modified: Tue, 12 Nov 2024 02:23:04 GMT  
		Size: 3.6 MB (3624492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1361abf28320c5940b76e04fc78133613a9088d535ec07d4e0da03fb715a7687`  
		Last Modified: Tue, 12 Nov 2024 02:23:03 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:8f4a634eb0e5b6fec9e3827eeb9eb9161126674f924b962c24cb5c7c0d87456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50577279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49170d13fb6237abfe6d5ebad353dc30a80089e3a0aa30949c7605b477c515d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9e5cb5648653b7931393711eee96e2908129ffb8e67d08c6b8445d6e254c4456`  
		Last Modified: Tue, 12 Nov 2024 00:55:24 GMT  
		Size: 50.6 MB (50577056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca67bda7e60c75e9899ca2b1d8df427c230a49496c777e8fe828f7ad0c5e39df`  
		Last Modified: Tue, 12 Nov 2024 02:01:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2e4e8e44493b20026d78e6a5ec8eb38ce9b9fba6e1dc3a5e928a46a2bc13b582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c629677d7f5c53995e44b3d0fff8c83d9b75d25d164e31c134437f6ee48f5b`

```dockerfile
```

-	Layers:
	-	`sha256:0f34b2012d352ea2f5dc8ac39804da4c0395299e93c6bbb394ede551ac274785`  
		Last Modified: Tue, 12 Nov 2024 02:01:53 GMT  
		Size: 3.6 MB (3621438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81837c8a0fce9e4431777e9b38b0d575f2b7d6adc1f0f19ba430adbdcbb0a302`  
		Last Modified: Tue, 12 Nov 2024 02:01:53 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:380444144166f6fc5839f00f2099b0bc4f1ab25f381808dce9cc75ab4c8df9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49559407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11819f4ee17aab5624aa064496423285e7adab18d4ef926460614056320fb9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4c50e8d8f6a17f2558bfa28ee5f569dd2c8ae9f47fcbafee2f205e57fabcaac1`  
		Last Modified: Tue, 12 Nov 2024 01:02:36 GMT  
		Size: 49.6 MB (49559185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b206bd1999f0e1a83353b8fa8659316e4895848146765526addb6771d04fe2ae`  
		Last Modified: Tue, 12 Nov 2024 02:03:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1136bab83b962403c93e71402cb279854bb13c8cddb83b15218d7be1df901f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37abdf8477b6788bd52a8961d9975548c390b0014450845e75cf1c968550205`

```dockerfile
```

-	Layers:
	-	`sha256:205038ce6f2f25524598b11cd8b05642b0429b5f431056377214155cd8e6a3ee`  
		Last Modified: Tue, 12 Nov 2024 02:03:12 GMT  
		Size: 5.6 KB (5649 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3c2d0ee32438e5aaa9a604e5f7dbf245f0cbbd302995479916f478b28735d5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7453fdde2204ae520508411750d211cf7825ccf65a6f8fb3307bcd83739ab5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b8382fbbc80bc625bdb4ce54b1d2e4cc425fc2663075ffb2c7f0721c8f035221`  
		Last Modified: Tue, 12 Nov 2024 01:01:30 GMT  
		Size: 53.6 MB (53555278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c48c1abf97120aeb6d3c2d62a6b0891ff9360c34fcafccbca2885d3d6993d`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0013ceb83a075950d798489aebd820e033475ed520b97d5ee09c1962acd7a1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9433518e1eaa2b6557d6c968edb0b1315a84301cba7de8b4f81ec5234d5ea2a9`

```dockerfile
```

-	Layers:
	-	`sha256:c709c71b38d209253b5624c224a43f55358d42d8807fa518d134337ac3e80d09`  
		Last Modified: Tue, 12 Nov 2024 02:22:47 GMT  
		Size: 3.6 MB (3628537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a533f1edf85148095bafe06f0afc615466316d52b71216b0866f1a122675a4`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:29ee76b00136241854f56f68a5fc27fa7737e26c64498d96fffb0e3a1a37bbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47938946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ee6a78dee897b2ac50a3c21b62c5de043bbb3cdbf6cdb56ef6ec306a3e6626`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01a1c376eda6239d331249175e9219276db8c964de72784f7003fc8fefff4629`  
		Last Modified: Tue, 12 Nov 2024 01:02:19 GMT  
		Size: 47.9 MB (47938725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6087496af574056c4c35437bfef7380d1acef81df928c69ee76a46b3965e8134`  
		Last Modified: Tue, 12 Nov 2024 02:21:16 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a6d61cdb5678f671957f0d8c757dcd76d227e7ac0010fa5d224cf82178e26f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115c3fea790a53330557d2781f3cc700f5e9c858afb49f50335bea34deeb82f6`

```dockerfile
```

-	Layers:
	-	`sha256:96f8dead49fbe9c0873f4097f28f017bfa31458d1105def8c18e92c5de8f50bb`  
		Last Modified: Tue, 12 Nov 2024 02:21:16 GMT  
		Size: 3.6 MB (3624009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b085daff0aad2f903159c8005ffc5a6e32d7f52eac895221aa1fa1339c3cb89`  
		Last Modified: Tue, 12 Nov 2024 02:21:16 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
