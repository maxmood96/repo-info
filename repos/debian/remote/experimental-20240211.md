## `debian:experimental-20240211`

```console
$ docker pull debian@sha256:58fb5bf1d3bc0b2dcd2a40474d2abace3f43f96c6e677251d3faa648dc7d86f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental-20240211` - linux; amd64

```console
$ docker pull debian@sha256:f4ef4757346e2bf9e46c2927a713fff36e432c97fb4428e015b87f782ca1adad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52336707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2cedb9e375207381293fca5acbf2cf707bf1516da69bbdf5a8016579dff203`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:27 GMT
ADD file:bd2b6594a7851e0983edf4382cb534b0f7d6c19c8ba5b3a8fd72364b790d4829 in / 
# Tue, 13 Feb 2024 00:40:28 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:40:41 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9bc32cb486734c012ca39c734855bfae01a0703c71fffd123222988a8938fefa`  
		Last Modified: Tue, 13 Feb 2024 00:47:05 GMT  
		Size: 52.3 MB (52336488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ddff30363be53a39b6bb09fc369b2e5ac6c9fea5d44374ce7239401c233bbd`  
		Last Modified: Tue, 13 Feb 2024 00:47:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240211` - linux; arm variant v5

```console
$ docker pull debian@sha256:9fed8b04d0552c53e97746a4ee5a358bee4116ee71706cabda0cdae85fc487c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49423862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab85bd50fd47faa12d45507901579b7150b74991ec4fb52330b5d201d81bc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:29 GMT
ADD file:c6463b88c118129758c28d371c98a296fabd1bf28529b98d9b17009f32c58ffc in / 
# Tue, 13 Feb 2024 01:11:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:11:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:96757a880e1aa0bcea47d20d9e344cae2b087cc8aaa16f7b3c868268e93bd703`  
		Last Modified: Tue, 13 Feb 2024 01:18:09 GMT  
		Size: 49.4 MB (49423642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be79066f3df19f946ad94a3452d417033c4f8a6dea0be83894321303dc9a0f11`  
		Last Modified: Tue, 13 Feb 2024 01:18:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240211` - linux; arm variant v7

```console
$ docker pull debian@sha256:da97ac04f2902031357e895cc53130103bcd53a64329d0bd0ebf62248f2388b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46929078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992e295afdf1c1e99c9d7dff09bedb467d51b9f773b7e9f2684c2e2da5072055`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:38 GMT
ADD file:757ae25421d966c7fe1362ecaaee1331a7b7963b397211de122e9b84e0385d04 in / 
# Tue, 13 Feb 2024 01:24:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:55 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:24315ce1e2b7fbeeb6e3acaec55b195e25b4c032102bfbdfa749bed4418f1374`  
		Last Modified: Tue, 13 Feb 2024 01:32:27 GMT  
		Size: 46.9 MB (46928857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ceebcd6b540c206943103e4af8545d6654411f63e8aff2d2733f327fc7df87`  
		Last Modified: Tue, 13 Feb 2024 01:32:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240211` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:988e994631d0343a9f5dfc93c6813a2b5bc953fee269b5dec736da50507a4f5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52195884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5b9bef1e5f4c52886fc88cae708d4ee404dc2dbceee7cde4432c948cf6be9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:23 GMT
ADD file:3f767395e4c9b86cbee1fca87b45219bc92e410a441304e5f528529aa6e0592e in / 
# Tue, 13 Feb 2024 00:43:25 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:43:33 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:93e14001ae9edd6e593eb18c455afa935d1a9f74e7c31bd2251abeb8c3c28641`  
		Last Modified: Tue, 13 Feb 2024 00:49:38 GMT  
		Size: 52.2 MB (52195664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d9b399d3a990ffa2cc7a62cea5882b8857366f7b02ddf2b0c5312349cceacd`  
		Last Modified: Tue, 13 Feb 2024 00:50:06 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240211` - linux; 386

```console
$ docker pull debian@sha256:fb1498e984f54cf4169848790ace5b2bc731eff87075b5429594f2e495be8608
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53166285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b2f89665aeb85a4731c2906bf9efab76e65e1e2f85d8ced7029de437b89f1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:07 GMT
ADD file:dfb0f9275c6543696053211f50b03852f21c22c0e54877fb81cd83b850d7999a in / 
# Tue, 13 Feb 2024 00:42:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:42:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:49f47060ab1ec69ef9caeb03c6cf7196c093445766d144bbe98a4b8a767ce7fb`  
		Last Modified: Tue, 13 Feb 2024 00:49:43 GMT  
		Size: 53.2 MB (53166069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f39e0b788c9c45c4f64bb0e3fc158761235e9a7e78669b92f4eab37d238b80e`  
		Last Modified: Tue, 13 Feb 2024 00:50:07 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240211` - linux; ppc64le

```console
$ docker pull debian@sha256:e9bcda2268717e352270c208a0695f3dce35cb3b05127b25c2743dad552f6b85
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6654b2bc030125104635a0db232175c3f214630596292496631b4e15cdc25abe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:04 GMT
ADD file:68ac050dfb10ba014b46971dcfe9f53251b3d9411cdf12507cd231f5bbbf6d78 in / 
# Tue, 13 Feb 2024 00:42:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:42:22 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:588ae578bfa6c02a9c1cffce4a14945b7f2b12f9d6780844b588d38c7df46d70`  
		Last Modified: Tue, 13 Feb 2024 00:48:38 GMT  
		Size: 56.2 MB (56237349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49a2837a3a9428b994ae88ac66cb439436d90bc7dbf93830699d190f1418df0`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240211` - linux; riscv64

```console
$ docker pull debian@sha256:07abbd394e94d28617c7345cb47aed9af4aa3e4efc3a4729bee3b80cf8f35aa0
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50535875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180c5700569b8ee9e2aff8cef26a4c7f84cf23df562ddebdf8b7304212a6bafd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:10:19 GMT
ADD file:0446fa55e9ff583a31907d973b22cad49c7e97ce651c21b99f7dd352822b9f05 in / 
# Tue, 13 Feb 2024 01:10:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:10:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:26daf40b5026d718684f79c8df1211b142380e8858eb72bfab47abfa81b3aab5`  
		Last Modified: Tue, 13 Feb 2024 01:13:35 GMT  
		Size: 50.5 MB (50535653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a51ff98bb8724925365acba64f077ff3a82ff551732753b80374f33008c81ac`  
		Last Modified: Tue, 13 Feb 2024 01:14:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240211` - linux; s390x

```console
$ docker pull debian@sha256:ca13bff6695f7ef22286d5d97abd0fe2c31bdf0f23fb575e1a562d2bb9f554cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51742591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba942c86478e9638a08224ea46146fdb7d7ad1ff286a5225aae32df4ce4c9a2d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:36 GMT
ADD file:ba2cb0aa84232154bae113547ad51991b49f209706d9ece4ee277fedea364ec3 in / 
# Tue, 13 Feb 2024 01:24:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0ee0bd49b211d30aa3bb1d78a78e94975d167ba11d42bb194bc72646320874e6`  
		Last Modified: Tue, 13 Feb 2024 01:33:10 GMT  
		Size: 51.7 MB (51742368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a956020dd8751679dddd57c2a2af56d517e84cdf5db672712d368329f7f2fdc`  
		Last Modified: Tue, 13 Feb 2024 01:33:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
