## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:5b7c058e335287071c5fea5a82e8eac420313ae18e9f7c197bd6498fd994768f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:49252a72ee7f580fb65beebc0cf02c40ad522a3d63c24632775028b307978246
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123988381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c94910fce9b566b875b840fe5c9675ae253658da46254f02b0ca92654698775`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:3f67740cbc1b7fefda4dc75bd2c0f0e76df9ae6b845f37b33cf8eea958403b6c in / 
# Sat, 28 Dec 2019 04:20:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:45:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:45:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f64e5c246a10532414f3b69dcf620cbf27337d8900089f4139ab3215186e02f`  
		Last Modified: Sat, 28 Dec 2019 04:25:14 GMT  
		Size: 51.4 MB (51358861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a40087c7676442e3d13e8a213aa17fb44a1cbab4d952197f09edac463f58edf`  
		Last Modified: Sat, 28 Dec 2019 05:00:44 GMT  
		Size: 7.9 MB (7919349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce8ee259aabe18e11221885897dc3fc3f8081c56a276bef858633277e6384ce`  
		Last Modified: Sat, 28 Dec 2019 05:00:44 GMT  
		Size: 10.2 MB (10182884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2980bfd4fdb4de40a047bf0530bc098ffcad6342b5a5b8ff22be79ed73e190a`  
		Last Modified: Sat, 28 Dec 2019 05:01:00 GMT  
		Size: 54.5 MB (54527287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b0faca890ecf5b683240c2dbfc86375d4ca3255996d4b2d5e7da11d7b5a7b6a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119167889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4beaa74ea5de80ed27c5cee446c4aca9e9417a30a15c28ec3e5b10aabfe8a6dd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:49:39 GMT
ADD file:b4c3e18bbf2b51c4f777d44bb8ef76a6fd78e8e9e057ffeb792fa8e041d3b40d in / 
# Sat, 01 Feb 2020 16:49:41 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:18:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:18:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:19:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1758f12059aa2a6d57dcc649233827a3b49cc528e7868081891f2a12944a479b`  
		Last Modified: Sat, 01 Feb 2020 16:56:07 GMT  
		Size: 49.5 MB (49485065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4449c159b35252b02eefe1b4989bc90d10d35fd6d17600ae5d662ba279c259ad`  
		Last Modified: Sat, 01 Feb 2020 17:43:56 GMT  
		Size: 7.5 MB (7494059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a6070fc56cb0dfa20ffac6472ce9dc9a8aead19638f495a62bff5206bf6ec7`  
		Last Modified: Sat, 01 Feb 2020 17:43:56 GMT  
		Size: 10.0 MB (9969002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5ef05714eb441ecaca79d450dfa2444ca3fe859d6c1080d660e208a78633f7`  
		Last Modified: Sat, 01 Feb 2020 17:44:18 GMT  
		Size: 52.2 MB (52219763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:abc0fc90a464e70b167f26ddfdcbf2a29906c92ea3bdfea0be6ea647f93116e2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113848683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5822dcdeac45bc81f23a8046aa5904f5a074e8ba22f71c8f7ffc52c8a60321e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:57:57 GMT
ADD file:ff4aac151f354dcf2159847b433d9631b254a18c30cb55390fe848c64ae989df in / 
# Sat, 28 Dec 2019 04:58:00 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:38:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:39:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aa5ecd1f9158499f6ccdafbcc35abc9cff760ff71453cf163442fd894809336a`  
		Last Modified: Sat, 28 Dec 2019 05:06:38 GMT  
		Size: 47.1 MB (47075322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29564c870b9ddbfdb14447cd65ce79e4a7d90599b8451e5102fbf34b5bbe13e`  
		Last Modified: Sat, 28 Dec 2019 07:05:38 GMT  
		Size: 7.2 MB (7232551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de02b8a9c8996450e899ce5c5cf642268569a23eacfaf79480c1237a0967c76`  
		Last Modified: Sat, 28 Dec 2019 07:05:39 GMT  
		Size: 9.5 MB (9528969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b277e09389ce7806d68c46268527690026db9abd4fccf9c2fbe89f2fc56f6d7`  
		Last Modified: Sat, 28 Dec 2019 07:06:03 GMT  
		Size: 50.0 MB (50011841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1ad465ece6b0be36a2aceb609195daa2abb6d9f5447f13d909224a17ac1c45ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123213873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0220f84d7210a24cbebda84f75a2a4f9eeaf8c7119f4ddc7a3c826283305d28b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:40:13 GMT
ADD file:485f0f88566199683d3683f547dbd33fa9cb4897121b104dd7c852162fa06cf7 in / 
# Sat, 01 Feb 2020 16:40:16 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:14:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:15:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:15:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f625aea7552a55d9aac253c9834ea6e645ae1e9d641ccec7e167585699e5d1b3`  
		Last Modified: Sat, 01 Feb 2020 16:45:20 GMT  
		Size: 50.5 MB (50453025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2bd511eb67667a40782667bc3dd7eb41f584de23c5a106085d2a1db980df9`  
		Last Modified: Sat, 01 Feb 2020 17:33:39 GMT  
		Size: 7.8 MB (7792989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f4fcee540ca05f3c8904722b70f13e10600fced1073a2612d04d995a93d210`  
		Last Modified: Sat, 01 Feb 2020 17:33:39 GMT  
		Size: 10.2 MB (10245802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5c01ce24c138f20821dc546f2dafea1d7baf1be4863e4de4f1957f18bb1577`  
		Last Modified: Sat, 01 Feb 2020 17:34:01 GMT  
		Size: 54.7 MB (54722057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:69fcb40163b6de6de9bfa86698b593352dc49b3fff1eb8250e37f087c06120e9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127689577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698c2a1dd6ba66d3bfe6d5722a3f3ec64db3940475990800dceca75901e43be5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:38:51 GMT
ADD file:a874cf7afdd9718652025bc1f81fdb39341a41d8e4974c1271c6a60c38827dec in / 
# Sat, 01 Feb 2020 16:38:51 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:21:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:21:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:22:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eead0407ee66421148ca3913bacd0ce8efc8ec3454d91b093f8e0c7a840cd526`  
		Last Modified: Sat, 01 Feb 2020 16:43:40 GMT  
		Size: 52.6 MB (52628381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da9f6d041b083f4fba44c0459502c661d52f0df7818ced468ac392766967d09`  
		Last Modified: Sat, 01 Feb 2020 17:41:04 GMT  
		Size: 8.1 MB (8093447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87a6a62880351b6dcbb87be2ef415bdaf2f887b295dab47c80dab8ad5608172`  
		Last Modified: Sat, 01 Feb 2020 17:41:04 GMT  
		Size: 10.6 MB (10615363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327cadcff72cda90b5fd1c9764a3569a81542203e324ffd68c0985c81a59eae7`  
		Last Modified: Sat, 01 Feb 2020 17:41:24 GMT  
		Size: 56.4 MB (56352386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b5178addba28c7053ca1aaf10f11809f8e066bc1596348937a2fec2730f235c3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134264845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9fd2fa97da676bbbfcbe9b786bcaad48eebae581da0b0feca7cdb06fd813b4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:19:20 GMT
ADD file:b4f9e68f81c696fdc52ed16b3080552fa23e19fe66b8de9cb3ade042aac7115d in / 
# Sat, 28 Dec 2019 04:19:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:34:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:35:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:39:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0127e22d45eca52f3501e5b68ef14e0d3a7c0c031138b56d8f69924604af15b`  
		Last Modified: Sat, 28 Dec 2019 04:26:06 GMT  
		Size: 55.2 MB (55181582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e72dbc0de56d75beeba9cd6882f85d47bb6b3077837bbff7414b67963edac`  
		Last Modified: Sat, 28 Dec 2019 07:19:58 GMT  
		Size: 8.4 MB (8353078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a10090632680817f5ee840a8157c3a412aa82b9db7e41f83c953b68f06651da`  
		Last Modified: Sat, 28 Dec 2019 07:19:58 GMT  
		Size: 10.9 MB (10945667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de2512f180efbf390aa5c580b30ec1231a51a986bb86bc7b1ce395d59903709`  
		Last Modified: Sat, 28 Dec 2019 07:20:29 GMT  
		Size: 59.8 MB (59784518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d4efd8f642ca901997f36c78eda44ed1ae1bbcaf5d321663369fbeced4c0d60e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121446309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c42a29541a54a65a95732adae6108d161f61c11baf037171dddbb6df083838b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:30 GMT
ADD file:ef81707ff6f9411444d40f7819b6103572f1c71599afd4c687f5262af6d30f7d in / 
# Sat, 28 Dec 2019 04:41:30 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:42:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:42:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:42:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6967537f6d685c8e7bce246638525934908340998b95e5baed55bd5e9805611f`  
		Last Modified: Sat, 28 Dec 2019 04:44:31 GMT  
		Size: 50.0 MB (50017657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5626baeec9661579acdaed4ea6587cae4c16df097bc274ac329b6422d405ed9d`  
		Last Modified: Sat, 28 Dec 2019 05:52:41 GMT  
		Size: 7.6 MB (7590139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69b710fc3f7e4f96daf59aa3255a7f810b677a869eedde6dc313330d76855e`  
		Last Modified: Sat, 28 Dec 2019 05:52:41 GMT  
		Size: 10.1 MB (10068811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb0c2c2d0d3cba15da991cde49579c040bc860db52909b9eb568b8bd8326b59`  
		Last Modified: Sat, 28 Dec 2019 05:52:54 GMT  
		Size: 53.8 MB (53769702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
