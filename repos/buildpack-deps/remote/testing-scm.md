## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:9b6b9d70b25d0562d51f31a57c39c3f0cabefbb69448c6a05c473654200b072d
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
$ docker pull buildpack-deps@sha256:0298a507e8663eb9bb31967392e363ce5c9fd0485c52dd880cf93f6edce44d57
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114069332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25252cdf46655cdb3950cf5908a374c0d429c164a9869f46cfc09c40ba42bd49`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:59:25 GMT
ADD file:202d96a6d5151b70202bd50e4082c0330e7568bfc44df705d81cfbe26c89ced3 in / 
# Sat, 01 Feb 2020 16:59:27 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:55:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:56:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:56:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:39368978c6fdc2e48756694e0bc73ec7a7db16e571f02e42ebde72a690544bc6`  
		Last Modified: Sat, 01 Feb 2020 17:06:52 GMT  
		Size: 47.2 MB (47233777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0657bdf1da7571cddc6b267a05d66156f8304de06b121de57f07153149a8ea1`  
		Last Modified: Sat, 01 Feb 2020 18:24:28 GMT  
		Size: 7.2 MB (7233949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4016dec180e52c4d1cb0efc60d7bce60531a204bae8eb6ff5259e9125ddc577d`  
		Last Modified: Sat, 01 Feb 2020 18:24:29 GMT  
		Size: 9.6 MB (9630242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27f7c38d457e4c5689d00dc9bbf26bd7e157f0c1a5d7ea962b11ae766b934e3`  
		Last Modified: Sat, 01 Feb 2020 18:24:51 GMT  
		Size: 50.0 MB (49971364 bytes)  
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
$ docker pull buildpack-deps@sha256:0d518e5bb7ed38649d15d72e06a735f17b496f740d9a002846bb923aee90eabc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134403777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76ac93e765cb2e39346dcc078b306359a1c2fe1c59ee971ab9be660b39ee118`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:17:00 GMT
ADD file:1a064022bd5caf45345b7a91191b82f0d2bb576e88e99652a4c3d68c399b1578 in / 
# Sat, 01 Feb 2020 17:17:04 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:25:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:26:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c80e92e9d0447b759db73a162ee40f56912d3ae4c251aa735339219ad9bc7a68`  
		Last Modified: Sat, 01 Feb 2020 17:24:16 GMT  
		Size: 55.3 MB (55316324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0367678cef47c5fbcdebd74948fd485de617cb36ea2d6182b1dfd3d5b1429b7f`  
		Last Modified: Sat, 01 Feb 2020 19:14:34 GMT  
		Size: 8.4 MB (8352503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc091c35bf183343a79cfcaaa09372d04e69e60e2bf829bb74249782b5c28826`  
		Last Modified: Sat, 01 Feb 2020 19:14:34 GMT  
		Size: 10.9 MB (10933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e665ecd4edbee998fa55d04d8629974e0da14b478ba821db4e2a9cda1bcf25`  
		Last Modified: Sat, 01 Feb 2020 19:15:22 GMT  
		Size: 59.8 MB (59801015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9404c912825554eee11294b1c46e95687a4ebec17ccc064af7391e81a9affe64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121671307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b415ba1d501a3a7ede49869fa5e87f920c34e36a378375d42358f3dec82dbe`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:48 GMT
ADD file:cce6a1a9e391072489b92618430aad507d896a0892b4ab746b46f65aeb50e142 in / 
# Sat, 01 Feb 2020 16:41:50 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:47:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:48:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:48:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:821c3e818de5d8d85868e03fa7647e09cacd5ec4fc251a32c8469652dc6a136f`  
		Last Modified: Sat, 01 Feb 2020 16:45:08 GMT  
		Size: 50.1 MB (50133126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf95eab022dfcbfcacdc7e34c79e2393c47272871cba3199d2f185d32eed6346`  
		Last Modified: Sat, 01 Feb 2020 18:02:40 GMT  
		Size: 7.6 MB (7592340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fc4d83f881a25a8f4d4dbecfe9212342061b813cb745e8c7fffaa872c5ce04`  
		Last Modified: Sat, 01 Feb 2020 18:02:40 GMT  
		Size: 10.1 MB (10141537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6114085d29f6feadc52b85130bb556649dad85820b38ee5a001c7aaf15842`  
		Last Modified: Sat, 01 Feb 2020 18:02:53 GMT  
		Size: 53.8 MB (53804304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
