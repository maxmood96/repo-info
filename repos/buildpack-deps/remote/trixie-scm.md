## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:2b72423bf2ef03b13da6e618e054c16609d1f9526450f6c1ee9eab6b073aad17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a34da2b9118ef97f6957c2679ef49fd464dba77f4ff6f319cc368a0208a8ccdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143152753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3a9948b9349fa7522fbdb1e093bc0e8f4c4f6e20eace5e7c5395e54a21e697`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:30:39 GMT
ADD file:6ca69a87b27d32cbf31b0d06d4e090d8fa6278a69ad5aff169e2671b9167ba65 in / 
# Tue, 14 May 2024 01:30:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:01:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6d60edd50c88b7fb0216608a7acfd61aba34227d9bd4ea28513f560cbacb654d`  
		Last Modified: Tue, 14 May 2024 01:36:46 GMT  
		Size: 52.6 MB (52640764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda240e3d830505ee3dd0bb459987e9bc62be918fc839670afe745737573ff00`  
		Last Modified: Tue, 14 May 2024 03:08:22 GMT  
		Size: 24.4 MB (24363073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab404979840e16d4b620530b1748adc71c5d5d3850f1acfc54d3f35d2c442b06`  
		Last Modified: Tue, 14 May 2024 03:08:41 GMT  
		Size: 66.1 MB (66148916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:77275acc369cebed2ac3723fd22cdc7f12b263da8c3381a70609935803189fa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136837464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453a58c76a2294e59c1b2c4e73f4f4588bb041668e49d938858c85a277f68157`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:50:00 GMT
ADD file:d955a729fc87dcc958dd6e2af15e9c9eb37297a3086e8d4bfb3be02e5a46d772 in / 
# Tue, 14 May 2024 00:50:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:20:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b7db74f3165f8c9d22b6ac35548933cd0a6f9c3a0ab156404e08d92183677b2e`  
		Last Modified: Tue, 14 May 2024 00:54:47 GMT  
		Size: 49.7 MB (49744769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ef049977e0812006734663b62c0c9fc04b58d3cc62704c1b6c49f5c37a6933`  
		Last Modified: Tue, 14 May 2024 01:25:14 GMT  
		Size: 23.2 MB (23221162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b3aaffe18defc6fb5b65541b97f325de0f6ff395c0157170cb2a196970c6a5`  
		Last Modified: Tue, 14 May 2024 01:25:34 GMT  
		Size: 63.9 MB (63871533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:713d81ef462eb90117c2defe4efdd2c817844c788c703bac7602e78153df9fa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131053765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f68cb253055e496ab3a0644deef6bc40b0b2130e28da625646eeba7378b8de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:53 GMT
ADD file:f86f34a21583f1f462e1edbd3cf67cfac5ca39220904cb41ebf8a535aa66a5b4 in / 
# Tue, 14 May 2024 01:10:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:473c2a5877d1215feb861519f5eecda926a82b16adbf75be52a3afb3b7198cfc`  
		Last Modified: Tue, 14 May 2024 01:16:55 GMT  
		Size: 47.3 MB (47252529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bbeaa0875c23824b09372aef266a9b567815e332fbcb1ff8d9f43e1bd2a5ad`  
		Last Modified: Tue, 14 May 2024 01:51:11 GMT  
		Size: 22.5 MB (22525435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f1700ad56ff9ea3accc7ee12afe6f68ad82341dac1e0c0e20c7ce70be3438c`  
		Last Modified: Tue, 14 May 2024 01:51:29 GMT  
		Size: 61.3 MB (61275801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b05fcd0fd05635fac84cc9d75373ef33f9431c907c5934523f0b6b6a94e7ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143378799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68cdd4af797c8d73986c185accc64176b7bdfb88622aca6dbc061b6ecff438`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:41:23 GMT
ADD file:16ea8fe4191950ef1f76dcd4d13001f5885d82028995463521ba098a1732d0c1 in / 
# Tue, 14 May 2024 00:41:24 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:50:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:51:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca9ad02c6b3d616bd616f75ac8933d247d3511de781f0e82d115f2da2ef04020`  
		Last Modified: Tue, 14 May 2024 00:46:40 GMT  
		Size: 52.9 MB (52912075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d5fc0fb6591f9243856fd83bae7bdb14d889ced46f2be7d5bbb4e11e08c4b`  
		Last Modified: Tue, 14 May 2024 01:56:29 GMT  
		Size: 24.1 MB (24095579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad29fbb033b8003c424dfd8b274e082af5d53de257b1fd10838051d5ee5c0a9`  
		Last Modified: Tue, 14 May 2024 01:56:45 GMT  
		Size: 66.4 MB (66371145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:af960e7fbcc350b416030b33b091261176ff589e0c9d44ac93c925188944b5d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146912555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a25b6cb5474b4fa90680c9bf6f990072a917c3266dd8bcec60ffc723c539f10`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:55 GMT
ADD file:4bde95af38666568e89de2e418b09573aaa93aeabda8b4b038fb8dd4661f1da8 in / 
# Tue, 14 May 2024 00:49:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:10:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 09:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:aa9ece0b8585431e0ff9dd469e342fd62709d864ae30e77f37fb1bf3ec9a010d`  
		Last Modified: Tue, 14 May 2024 00:56:55 GMT  
		Size: 53.5 MB (53536613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f9e274ac15171ba10dd426a1e18136992a1cbefae3b1fb5dd8aec53b2b834`  
		Last Modified: Tue, 14 May 2024 09:18:45 GMT  
		Size: 25.5 MB (25463473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8e105b62fa29e13280968280936d0a70ee9b38fa07dda91b02c03210439f7a`  
		Last Modified: Tue, 14 May 2024 09:19:07 GMT  
		Size: 67.9 MB (67912469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6e04c5d621e0a6a9f69dd80fe0964942116ff2e89755c43ffcbdf67b3171c2d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141573043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c38199a3555ba63d7d336f29c424649fe338477854214bc9765d4d9e0a9407`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:17:59 GMT
ADD file:1f0b17ab026fdd934751367c5e083a2575e1992f41afa128d34d6e389a8c5e15 in / 
# Tue, 14 May 2024 01:18:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7da4c62a06fc3bf1f9a9122b195e061bf68ab1f32de26d020d80c1c991a36658`  
		Last Modified: Tue, 14 May 2024 01:29:28 GMT  
		Size: 51.5 MB (51533695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fe200f683c88194ce811b89cbd98c717530eab86f223b53cd1153f36e125`  
		Last Modified: Tue, 14 May 2024 11:47:11 GMT  
		Size: 24.8 MB (24842389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9540b2188576148a4180ee4eecdc60d183310d6da50fd577a6723544639ce191`  
		Last Modified: Tue, 14 May 2024 11:48:04 GMT  
		Size: 65.2 MB (65196959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:32baf20c2d82f32809fde80203a18549aedec9c918ea9231c91731c20d02c09d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154745159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328d204a07456036376484673dc1e889869487a0a8e0089bd5558e1871d40c52`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:22:12 GMT
ADD file:b70e585933669ccdec908ca881e353f753c7360b65d8e56151a5cbbcb563650e in / 
# Tue, 14 May 2024 01:22:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d4ffe5f5ec6419780cf58ebdddd161cfcaf20013a69d7e07f3c216e113c443e0`  
		Last Modified: Tue, 14 May 2024 01:27:42 GMT  
		Size: 56.5 MB (56531499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa06aa5a174624eb14398575acf70b77dbe1513cbc35be06ab880a2fc047df6`  
		Last Modified: Tue, 14 May 2024 07:14:06 GMT  
		Size: 26.5 MB (26502688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f169ecdc07bedce89e0b8cdd6a09e00cecfd1b05f36ab6b7bcff1146b596777d`  
		Last Modified: Tue, 14 May 2024 07:14:26 GMT  
		Size: 71.7 MB (71710972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e5c1a3992746e6832041bee53a8c59e76b89adf2545474dbc4535c28314d24d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145292706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e09e7693ba380c030f007b4b0993daa21b667a828f32c97efc09b9770fa9f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:22 GMT
ADD file:bfed51c8ee231f326b9e395ed053f8f43d279b5417c51e35c047e68700215236 in / 
# Tue, 14 May 2024 00:45:25 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9eb3c214a4e6341fd5bbb5ec28963ebea467eb38d93ba7fc51ddc4ab988ada8d`  
		Last Modified: Tue, 14 May 2024 00:50:04 GMT  
		Size: 52.3 MB (52291053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bfa3e7d2d727a0d58b3db18761fb57fb587d12199cb7efa64c42f48041922`  
		Last Modified: Tue, 14 May 2024 01:32:03 GMT  
		Size: 25.5 MB (25548180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d91ad2f2796294bae2dc78cdf1b09c417cfe0512b71fa44701011368d175c`  
		Last Modified: Tue, 14 May 2024 01:32:19 GMT  
		Size: 67.5 MB (67453473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
