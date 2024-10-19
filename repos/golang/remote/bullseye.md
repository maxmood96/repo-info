## `golang:bullseye`

```console
$ docker pull golang@sha256:f99b93ea4c5fd245408af86e02270aebdfbc9aff0568944909702d60e420c8d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:67e3899b67b6c23491e4a4a8b36672945c398cd4345ad4be8cd9762d6e3b5a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285545975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be600d787e1a38d14e8dee28fdf832ecb73920c83d795fb03fb2c8af26283f5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d056e4519a5022985912b1c587343a678840c1345a2f22a723a659cd6130005f`  
		Last Modified: Sat, 19 Oct 2024 02:53:04 GMT  
		Size: 86.0 MB (85971223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1f1163629431c9f488c4d6ff6afb5c73021839723b50bafe245663ad3d9df`  
		Last Modified: Tue, 01 Oct 2024 22:18:51 GMT  
		Size: 74.0 MB (74006382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e48089bb45b7014562cbb61d57f4e218c78fa271ef14fb3efa86de62e286a6c`  
		Last Modified: Sat, 19 Oct 2024 02:53:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:c7cd71d6ee6c143300e723f50a2f10073fac5e32a454d4e438e01411bbf2aa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10310304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3025a2796931ee50edec2b49446cbe0e0b9dbc38378898178ff026c2aa8d4`

```dockerfile
```

-	Layers:
	-	`sha256:dea49fb8a72e56ec5d908eadc60926788a2effabb0e076c253ecc6a7dbd1ce5b`  
		Last Modified: Sat, 19 Oct 2024 02:53:03 GMT  
		Size: 10.3 MB (10283837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751f2bec91ec4e9ef12627d600fe696abf707b1a2829d996784244c719e95679`  
		Last Modified: Sat, 19 Oct 2024 02:53:02 GMT  
		Size: 26.5 KB (26467 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:ae524f92dd59c4f10146fbdf2031aac55c913c086ce47f31fcc69697f3783614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252794656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b4d5917c729584e4872fb3a81abd0fd56b8bd1e7e74734ebab9dbe810853a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Oct 2024 17:43:12 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Tue, 01 Oct 2024 17:43:12 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59299672bdf285da5ac04bba51bc8d7065d56d84dc91659b563a337a1ef7326`  
		Last Modified: Thu, 17 Oct 2024 03:38:03 GMT  
		Size: 14.9 MB (14880063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39efe447d42646f3185dd530992915f4ee5284d42835f09c0a8c04ba06ba134`  
		Last Modified: Thu, 17 Oct 2024 03:38:18 GMT  
		Size: 50.6 MB (50618781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801a5c06e432e106bb520490b3d4c98dbb729cea570c6495f5f07fe3b0d08be4`  
		Last Modified: Thu, 17 Oct 2024 13:16:43 GMT  
		Size: 64.9 MB (64892674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda832285c268d03f9079f25d645da4f232d333a236aca4f5406f4294d01f183`  
		Last Modified: Tue, 01 Oct 2024 22:22:37 GMT  
		Size: 72.2 MB (72161385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d57ec9543fcd77bb29bf2857b0b52daa69307f3a48bc17669f4b96ed6ec093`  
		Last Modified: Thu, 17 Oct 2024 13:16:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7ce22e575c799a7cca2f47735b93da0cdf2a91bc38984793d8981c536a78ba71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10089535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5273c549894f8fb394c0c76175e716621e4645d091b29d67601bf6a67468ebb5`

```dockerfile
```

-	Layers:
	-	`sha256:57abc6b5bc6b0172fe329b3a6566a373fb83334625100512668188ccf288fe7c`  
		Last Modified: Thu, 17 Oct 2024 13:16:41 GMT  
		Size: 10.1 MB (10063052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f914d29b6bdf693697cbac1c7e5c92cb524ce2771da28fb472538e6ef1a39d41`  
		Last Modified: Thu, 17 Oct 2024 13:16:41 GMT  
		Size: 26.5 KB (26483 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2d1d810e01145f9cbf9f13a850be30046961d2f7e321896018104224adb350e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276341908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562e9978390f6ee147b4628a8edff844fa15eed00482d6c5cdb5a66815c3c8bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe97e6654820c195f58da24c03de7d8f33a297eb7c6cb4b9d259eb51a1369fa`  
		Last Modified: Sat, 19 Oct 2024 06:57:32 GMT  
		Size: 81.4 MB (81382275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a00ec5f007d0ae73647c82b7d81d98a44fb7d073d06e633d656bca79db62a`  
		Last Modified: Tue, 01 Oct 2024 22:22:17 GMT  
		Size: 70.6 MB (70644133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f56fcc26e132b17e4a3475c0698897a33ef39784a5cc5baa326de73402befa`  
		Last Modified: Sat, 19 Oct 2024 06:57:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ba7b65cdc7f8942b69a65964132a6ec2d854575483eaf3ccfc2f27d127a4352a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0741964fd71d486d6cc3d99b2bd15f2c3b4bb522088b233bae6a4a15667a0e6f`

```dockerfile
```

-	Layers:
	-	`sha256:ced706de09d5a4283d19a03f3e6913ad98a1a0dcb850a15dfb22b6396a789e50`  
		Last Modified: Sat, 19 Oct 2024 06:57:30 GMT  
		Size: 10.3 MB (10285435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09fef967632a085498002a0e40df4b3aaa587f21c4dfb3f18ba6b718ddbd5cb`  
		Last Modified: Sat, 19 Oct 2024 06:57:29 GMT  
		Size: 26.6 KB (26632 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:e6fb5f574db4851afbac355497c19e5f455df1f8d6564ed5d6d14cf51e2623d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287650921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae34c5925ea8dc1977d232ef8f376598197b1d66a526b9cfd6110e488f3ee582`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOLANG_VERSION=1.23.2
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Oct 2024 17:43:12 GMT
ENV GOPATH=/go
# Tue, 01 Oct 2024 17:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 17:43:12 GMT
COPY /target/ / # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Oct 2024 17:43:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d988574216ea21c2f3663e265b982dbde4c9e93258b6bcc9fd4ea3e5ab1c0326`  
		Last Modified: Sat, 19 Oct 2024 00:54:49 GMT  
		Size: 16.3 MB (16266312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaed38ae0fbef304c5263999f070de89cac39bc284c57eb71df4b52535defd79`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 56.0 MB (56028643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3b8ea2ef30ad6da6a62fa0971cb2d1bc21e5af9dcd9c05a2f6c06c57223b70`  
		Last Modified: Sat, 19 Oct 2024 02:53:02 GMT  
		Size: 87.4 MB (87397772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d4de23fe72666a7f8131049dc36e9aa2ba3bb48644c246b44b0b9d60e95bfa`  
		Last Modified: Tue, 01 Oct 2024 22:19:00 GMT  
		Size: 71.9 MB (71880213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e48089bb45b7014562cbb61d57f4e218c78fa271ef14fb3efa86de62e286a6c`  
		Last Modified: Sat, 19 Oct 2024 02:53:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0b97250ccd0607010422b303213adfa9c587f18a8dbc98e0ddd4e5811e0e8dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10300055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2096c4d32f0553b8d6bdc05b1778961a4375d533561bff13bc4fc3d17ee522f`

```dockerfile
```

-	Layers:
	-	`sha256:71add33f5a027f3e591d7b18154648e0310d3aaa428df21eb358da0734d2effe`  
		Last Modified: Sat, 19 Oct 2024 02:53:00 GMT  
		Size: 10.3 MB (10273623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe8a1d62c534a3c8abbf92e8a81f39d4cffa6e20f39e56759ffed063eb025e2`  
		Last Modified: Sat, 19 Oct 2024 02:53:00 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json
