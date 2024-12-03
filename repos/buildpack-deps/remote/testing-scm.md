## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:9283a18cceaf203845c1aab87d81076f8d63ecd3478c2bc04376b3e969432445
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:da06b24525cf008d45f41cb668247eee87a08689df068a618d546916d6ae1c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139771011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ca6d8dd9a27942e7de592f7688c5ce9541beb0071fbb2c608ceb2bef3f6f6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b5387da4a2f31c146885e44d705069d7906eee138ab3588a9fee7bcae723e`  
		Last Modified: Tue, 03 Dec 2024 03:17:15 GMT  
		Size: 67.1 MB (67058436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8a576689048442f9285b1e2d3b8e70de8ffdfb4c20c56d6e70985784cd861a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8be949d7ff95df28359fe769be1e7b26f6f2bd935fc6ca92743ef514696ee24`

```dockerfile
```

-	Layers:
	-	`sha256:d392955327241dbd4fa732bf7f7bf2f671035b7dff2ce50e2a7fd0802cc79306`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.7 MB (7673471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f3b7d42efb398b3cb47bbe501e8f1d88b26d69ba97707db98f4be1d3a213b4`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f58998c164b872a995e8c2488d4449c575c973afdd5328339dce33bbaecbb6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132678369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996871804936b7a5ef88a59edfb5ff11a638889c5c06ba22cac89fae0dcb7aaa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bb9243d7017922dcc62de48c63d8cfb54c3c1e685c3e38d7cea429218c0e`  
		Last Modified: Tue, 03 Dec 2024 08:42:18 GMT  
		Size: 64.4 MB (64402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9eac8d18f0d619b921e87fb696ec7ddd1dcd909048886f90f96abca7fef946bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4899ab3a5d47d295306707e3a125b9526e97ba5ee2e8421e14431b21b28ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:24d68fa4daa45f024376e555272bf77b2c06ea5f777b7d93ddb7878d49d60ecb`  
		Last Modified: Tue, 03 Dec 2024 08:42:17 GMT  
		Size: 7.7 MB (7672931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14de663ae0734d8f5151fdf3a515dceefedcce57432d1cd70a5f5e9a49cc37c`  
		Last Modified: Tue, 03 Dec 2024 08:42:16 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b6766c9d485c53509f2a273917a0180e17e320c8c343a33328cf84df6c06e49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128092993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf45ac2a1324984e287a93dea6694fe11f741ab7a7cb57cb719e5c0008bea1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:da23906b82d0da338b0e507d1bef5cf2747e130d745e77708e8f5279af9a4764`  
		Last Modified: Tue, 12 Nov 2024 01:02:46 GMT  
		Size: 47.7 MB (47681766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b00d9d0a43af35aa09caad4b98ca01f5b7a33e4efde2bc19aa6be0499f216`  
		Last Modified: Tue, 12 Nov 2024 16:02:34 GMT  
		Size: 18.9 MB (18945100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec7eb745d8411abb388ce98360bbd90d28cae91d3a58e4bf19484532efd8c5`  
		Last Modified: Wed, 13 Nov 2024 07:41:04 GMT  
		Size: 61.5 MB (61466127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:973f4e53128e19f1f9266d9cd0f2752ebabc1e8631cfacd8e89115f78f77bed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a59900152de20035a985374979d3abebc48fc6bdc88ea158ab266383f35c96`

```dockerfile
```

-	Layers:
	-	`sha256:542109b2c54fcaa00863e4dadc9f26c5bd33f11aab7bb8aceb900e6d975a5ab8`  
		Last Modified: Wed, 13 Nov 2024 07:41:03 GMT  
		Size: 7.6 MB (7615736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:520375c3be7d6fabf47e01d871addb473c014dfa6eaa9613ce94f8e357714bcd`  
		Last Modified: Wed, 13 Nov 2024 07:41:02 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e68ba4155d2ba86fde8d389332d35fb57b219ab388c52083fb2444efe918ea4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140474976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e64285bc4c8d47537d83d55000ab224324b279033ab7b8bc92945167abfa6f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27cb33ae9e17116eb9be8382614725b619742aeedfb992b4bc26c5d5efa717e`  
		Last Modified: Tue, 12 Nov 2024 11:17:43 GMT  
		Size: 20.3 MB (20252075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb08f62c15bea658c57ae9f96fa28c800a3f5d9e56db394a67684608bb7764`  
		Last Modified: Wed, 13 Nov 2024 02:44:37 GMT  
		Size: 66.6 MB (66552924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ffcccd6c472db2ad16e7472dde5590c02d9ae19978f59bb583c24f2d9d38810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f591844f361615941dcdc296cd5300c1afd784c436186b2cd88cb1d7213e5a5a`

```dockerfile
```

-	Layers:
	-	`sha256:318f9c03404ac143438a39d4002624ef9668934df3300c4c327c325e35130c59`  
		Last Modified: Wed, 13 Nov 2024 02:44:36 GMT  
		Size: 7.6 MB (7626750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794ac960c7af0f044e1c0e47cb50a4e5b4790c29b0b6a81c475c748bca1007bf`  
		Last Modified: Wed, 13 Nov 2024 02:44:35 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:719ff7c42eefa5f6811c72f3d92c194797cadf5b65455e346d3cb3e9b7705616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143544476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e3ad359f205a750b81d425ca9d2f51cd5eeefadb8cd309a411bc9397fd7e21`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad782586fddb10041571d568c827bae913dd109647631cce2fe893ecfe4b9488`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 68.9 MB (68861394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:535718f08215a34be3c30316648e76a757427791ab2fd9e70495b1e6a5e58b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7675497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa66fa78d05f3be959bc718b8f26030aa9c1a00679251a79660446336a3ffee`

```dockerfile
```

-	Layers:
	-	`sha256:d64db0dc614cd414a9d0e4644feae150e0f1e8c7eda3e0b58ee2612315e3f67e`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.7 MB (7668205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c80bd9ae34e9602bb84c05a4ddf8a0caa783edcbe6ea469738ea67b68efdc55`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a57aad00feecb8edf6a531a3b2273b38be5782fd4b5c2fa686bd3ffb7bb477d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138504731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7cb8809cd8d0bb5c836f77e402319e5b8174742ad7ca2deaac8446abc8c79f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e85824c3ce994136e0b1f6545ca38052c56e3faf7dc4ab5102ef2c2e357cee02`  
		Last Modified: Tue, 12 Nov 2024 01:08:01 GMT  
		Size: 52.2 MB (52200415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c4cfa8a0eedb22460a31984d56495095c0e6d072ab4be3aa70aec30584cf7`  
		Last Modified: Tue, 12 Nov 2024 18:05:03 GMT  
		Size: 21.0 MB (20951814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174684d328adb3f37db85b256c1516f8c1ae147bdb5b13929af1a4f6ef492496`  
		Last Modified: Wed, 13 Nov 2024 02:09:28 GMT  
		Size: 65.4 MB (65352502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aeb383292ed98f4e95e7bed23e796ac6667a5b32d7643ec0320d200b94f1584d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7d0367030e0511dcd2d0554cb412a467c40ddd6bcc39f900c52198c48b5a46`

```dockerfile
```

-	Layers:
	-	`sha256:a57a9024738cef4b7c03619301631a79b8697a908e20800b4364f7d9cab9d9d9`  
		Last Modified: Wed, 13 Nov 2024 02:09:21 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:29106e083d3f0884ff2ab67cab04de54b2948f989c84c1de72a1ceb5d72f2900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150416706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ec1fbf43792ca3ab0d994b9fbdf8d4c8fc7e96b90202e42e6e6c01520a25cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7a5f51f1d75eb637e939fe2c1d001071a9ffca3db92bd98f0f44b1414ddf061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05632c83a4dc663ff459ace817ccabda153cf61714e31816283eed707acf41`

```dockerfile
```

-	Layers:
	-	`sha256:e80dad17cad41492690720cb23ab6f99daa18133ee238fccb5bfbdfefd17ab40`  
		Last Modified: Tue, 03 Dec 2024 09:44:39 GMT  
		Size: 7.7 MB (7679219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413f4d207e490cadfa1567ed05b98441f383ecc08e32f7c8d9168196cbb75d3b`  
		Last Modified: Tue, 03 Dec 2024 09:44:38 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7cbdb5aaa9bdb372290824b75edeb47013f021005307c350766138665edeb373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141874600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a0fb9ae5e7d29b1b0cf491d5393a5ac639936cf966ffa23da517254253e92f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0425f6ff87e23ba6d559005a68cf32aede99d5bc0259e82af81721ec006b580`  
		Last Modified: Tue, 03 Dec 2024 07:56:17 GMT  
		Size: 68.1 MB (68095081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39a2f7b3b1fb4e73530d08d088bcd30eafd6d5d786bc9387b653d8f8d8b3ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c702e9c9410935d4299af789c96c665239bfb53818cf765a6699f89a9cca41`

```dockerfile
```

-	Layers:
	-	`sha256:a366d37dc4c5fab3169fa8005fbfd07ec0cdacfc63c176b0074314ab29054942`  
		Last Modified: Tue, 03 Dec 2024 07:56:16 GMT  
		Size: 7.7 MB (7673077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d3948af2dd637e8a6e5a87efaa2a0c83e3771e6c96a7300299f8a4fa0515d9`  
		Last Modified: Tue, 03 Dec 2024 07:56:15 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
