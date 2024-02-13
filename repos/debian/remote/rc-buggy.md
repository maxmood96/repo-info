## `debian:rc-buggy`

```console
$ docker pull debian@sha256:3739b0859aa503894429c277dbc70437e9932685f56fe239874fad6655866d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:38b02150e6699d140b55e9e5e2fcab084ace8530c76c7066710e8e03dabc8923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52336711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70659a2736903efb38424d9c2b17e444ae4cb20d405459af91c9643320fe7092`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:40:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6acaec7a3504d0aa06618a7aa894352660b5a21ac27aa9b715ac32d636a0637`  
		Last Modified: Tue, 13 Feb 2024 00:47:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:f30bbd20bcf9a5be6269ae127043fc3edbd6b8d7e89ccc68943fe402854c63c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49423867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d1f54d9a777f3487ba1c7846355d8a9faab55f5e2829cb8fe36ca159e388a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:11:51 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c11058550533c596aa9f193e92746ae821e22a43d242b10f0b014c9189d4c7`  
		Last Modified: Tue, 13 Feb 2024 01:18:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:ec1a79ac170b716ec9b92d72faaab83782bcaea1a0497a07607b5012185903db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46917786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fa98029f37bf2d953e5840c53d091c9cd698527738876c2b8fae6dd512ffb6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:58 GMT
ADD file:bd90d0f1ca5c36a5e1904d7ae20530c307bdd6b9e95969d77a5ddfcc2a05a5a3 in / 
# Wed, 31 Jan 2024 22:46:00 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:47:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fc855b34c99f9eb7f5014e33574cd598c0da1401f1cd9ed077eb716baeb3d1ff`  
		Last Modified: Wed, 31 Jan 2024 22:51:47 GMT  
		Size: 46.9 MB (46917561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2e9657b73dd60d2c78f6bbb0298822d358d02198bc96ccad51b28d58ac9a8f`  
		Last Modified: Wed, 31 Jan 2024 22:54:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ff133556e77e1239454451db4510fce60d0198501edeb72e7a9d10844d28c931
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52195886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a1d250e6980e1560a49cfb8908c29b33c6fe1da3c08faa01037af72d541d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:43:35 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e8231a773c5fdd4754b0eb403399321dde58a8b7d8a26777bd178ea863e26`  
		Last Modified: Tue, 13 Feb 2024 00:50:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:9c782b7c91c11bf6595dda67c97e979bd886f8684db3baf28ac4a3e6d937fa8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53166292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d533392158b2ab576700e9dca5ad0a4819daa844a7ab75075b03cc0e9336883b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:42:22 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585a6f765fb1a3d4ef83b772cda14ffc2c0f2e047f4c9fe3f1972b0fa2e39fac`  
		Last Modified: Tue, 13 Feb 2024 00:50:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:bf8ead425e2d2146f6757613558bb40401d47217d73c801ee8e236d77a95289e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51406790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f07ee62772d68f1d612c246c93a06cebbf0e861adead14b7911b8b51ffea6ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:21 GMT
ADD file:6a1dcc04909356575c7d849b10872921731a30bccddfb53ba49ae8626652a273 in / 
# Wed, 31 Jan 2024 22:30:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:36:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5822a20b82218747f0844b39d5a436f6742aead15996aa69a1122f629a606a97`  
		Last Modified: Wed, 31 Jan 2024 22:41:46 GMT  
		Size: 51.4 MB (51406564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f12b0952a67b767f0a97de159a6148cff6a2af2032c1be8fa0563d9821a90ca`  
		Last Modified: Wed, 31 Jan 2024 22:47:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:d510556956213a23491b496a2ba326533735996bb3107779522eacfc14f4c782
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f705ded9b80808453ee4b66d8af053c22fa56c975b4c036da1ed97212f300a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 00:42:27 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8e1acf6bebd4e0df6d200c3426cb75b04293eba4c839a6deae3b9c2c00c81f`  
		Last Modified: Tue, 13 Feb 2024 00:49:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:ed84164bec5b2de420f7e6541ffbc804ec128b87be603a53aedd3ce5e89abd90
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50535877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9901293b2cd4d94d790e6ea74a86279ebba9c5b8c4a8a82daeb9992d00fdc92b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:16 GMT
ADD file:b421fdf9092f4ec73d99564dd5502ef1d3668a7a691ba3bf1dbac96a04dc4a5e in / 
# Tue, 13 Feb 2024 01:09:18 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:11:02 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:dd7397a9685010df855591550ae6ac222e43aafe4aa8f629b13f53ec98a94bff`  
		Last Modified: Tue, 13 Feb 2024 01:12:06 GMT  
		Size: 50.5 MB (50535650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c614d645976d059192910cf9254a76b42a2820776c8f034ce6449394e9272bb`  
		Last Modified: Tue, 13 Feb 2024 01:14:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:229bcf83796b77db66b3e1e9add0b0c2045e167057e528582b7f059a4d707b11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51740799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee654ebd2a9fa087f3c1e1a122228fb22797a3999ce76673c50b7a0e5d746b92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:08:13 GMT
ADD file:080442a095efb5073711680e1deba8957cf0f0b56df25b98ee50a762eb11be94 in / 
# Wed, 31 Jan 2024 23:08:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:83efec03ab43dce66d67adfca29d07dc60c49e276fbb445b9c7dab67d2879a9e`  
		Last Modified: Wed, 31 Jan 2024 23:30:22 GMT  
		Size: 51.7 MB (51740575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bcd0e3404b4e2726b93ad61ccc57b301ad89621b551521fe57c228732b18c2`  
		Last Modified: Wed, 31 Jan 2024 23:32:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
