## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:e4ff446f3d3d92269b7e5ee7a1042c2bee25f7e1f7ee3af581f7bc4dc988b2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:151e4475069ab798e2d58d8452694e09981c467e55103210c5025b9eb0a42ad7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.6 MB (732593978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4233fb200e157334c9f89a7aeca1e0c8aadd9bcb8d4edb9ee21e3ba1719e3a2b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 20:28:44 GMT
SHELL [cmd /S /C]
# Wed, 12 Mar 2025 20:28:44 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 20:28:46 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Mar 2025 20:28:47 GMT
USER ContainerUser
# Wed, 12 Mar 2025 20:28:49 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 12 Mar 2025 20:28:49 GMT
ENV MONGO_VERSION=7.0.17
# Wed, 12 Mar 2025 20:29:11 GMT
COPY dir:c1f7dac9e27c15774292d02d4d27685640b385b96631f12dcad5ed2ca42440dd in C:\mongodb 
# Wed, 12 Mar 2025 20:29:29 GMT
RUN mongod --version
# Wed, 12 Mar 2025 20:29:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 20:29:31 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 20:29:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f6b73a47370a9bfcbbf55e24a9fa8b8063a58ba7054d7e18641ea358ab993d`  
		Last Modified: Wed, 12 Mar 2025 20:29:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1850f587e2231a648a9516d55d6e18dc1ca2eb0e19d96c0b3283882044a9ba`  
		Last Modified: Wed, 12 Mar 2025 20:29:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1319c5bfb40a97afe2cc5ad760fed4c85b65c5fafc9f8e72114a5483f5eede`  
		Last Modified: Wed, 12 Mar 2025 20:29:35 GMT  
		Size: 76.8 KB (76810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c05259c17d68988cbd3cc791912dc290e9ad7e7a2aa2f542769c1a8e614532c`  
		Last Modified: Wed, 12 Mar 2025 20:29:35 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183fd4bc9f45f2e088c0e638d14d1279c4297e4c4bcdbb11ae713c3e1a719256`  
		Last Modified: Wed, 12 Mar 2025 20:29:35 GMT  
		Size: 275.2 KB (275157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3933fff66e79c9f6f26420e964eb409ee2419f25e129d06196521abec914a3`  
		Last Modified: Wed, 12 Mar 2025 20:29:35 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f586c68a0ec5cbfe14ac0ef169df4ab70fcadceb6c5379c394a81ec23925d9f`  
		Last Modified: Wed, 12 Mar 2025 20:30:23 GMT  
		Size: 611.5 MB (611461888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901b6dcd06fe0dcec7e4c047b61e0d9dd4ad2810626689cf9becbabff71a20b6`  
		Last Modified: Wed, 12 Mar 2025 20:29:34 GMT  
		Size: 77.4 KB (77380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1448ab61c18bff0ecedd2883b57c16fb92e05eb379a35acce0c6b0dd75c62581`  
		Last Modified: Wed, 12 Mar 2025 20:29:34 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277e58262d861e3db27be5527e5852c21affa426e7964872577e2223a21d16d1`  
		Last Modified: Wed, 12 Mar 2025 20:29:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500a098ab6204e7779dca265055b2aff46c694e47a1ac03a67673db03fc5fbce`  
		Last Modified: Wed, 12 Mar 2025 20:29:34 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull mongo@sha256:0973671d11b10d00a27ac5b78b59fd6bfc3a31d0989b68c537b1c905c7d7d49c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.8 MB (718803463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10f8e4e5f03402d10b1c6d1dc904bbcd1facb1d2241d52c6b0a2aa55b90e9e4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 20:21:45 GMT
SHELL [cmd /S /C]
# Wed, 12 Mar 2025 20:21:48 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 20:21:51 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Mar 2025 20:21:52 GMT
USER ContainerUser
# Wed, 12 Mar 2025 20:21:53 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 12 Mar 2025 20:21:54 GMT
ENV MONGO_VERSION=7.0.17
# Wed, 12 Mar 2025 20:22:20 GMT
COPY dir:c1f7dac9e27c15774292d02d4d27685640b385b96631f12dcad5ed2ca42440dd in C:\mongodb 
# Wed, 12 Mar 2025 20:22:30 GMT
RUN mongod --version
# Wed, 12 Mar 2025 20:22:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 20:22:32 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 20:22:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890cd41c58f9bbf0324d00500f4f5ae107ffc9926113ad6f294ec38ffe8ede19`  
		Last Modified: Wed, 12 Mar 2025 20:22:39 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fc6fc45db6f71fae8a9d1f81c60ef7ba7afdb46c62e20b4057398ee5a0ed3a`  
		Last Modified: Wed, 12 Mar 2025 20:22:39 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9aabee9c201d699d94a23e711a68c91dd9c3176ba54fdcad1f68289f11d16ab`  
		Last Modified: Wed, 12 Mar 2025 20:22:38 GMT  
		Size: 71.1 KB (71072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ffd17cc7152486ceb407b2bcc776352d0bf418f133595ed585ce6998ad9662`  
		Last Modified: Wed, 12 Mar 2025 20:22:37 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16676aaf196626791b5141a318c9bdcb37f29a6a7704c7e3e6b38e30e28ef5c1`  
		Last Modified: Wed, 12 Mar 2025 20:22:38 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04e607a7388b50656edf81ffcd0175e5d66e3a4433ea74317e81ac0ec372c41`  
		Last Modified: Wed, 12 Mar 2025 20:22:37 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fef8b36b50ffc3fd7fc4ae3cefb9927de2c203880a4316098ad84f92d0b5d6a`  
		Last Modified: Wed, 12 Mar 2025 20:23:24 GMT  
		Size: 611.5 MB (611461850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e349bef089057104d1ef682b6a64329569392a14094b5cdb4e781827678a413`  
		Last Modified: Wed, 12 Mar 2025 20:22:37 GMT  
		Size: 80.4 KB (80396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b0af217833df229b2ebfc19bd807efd43b4a7f0abb91255be84bf9654fe524`  
		Last Modified: Wed, 12 Mar 2025 20:22:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9d78a724a01e0aad055f8d6ff4ea359a21c8136ef4693137d848c99bd6f3cf`  
		Last Modified: Wed, 12 Mar 2025 20:22:36 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8ccc26694239658e014fface4adda594c108843b6086de0715f368a505b4ba`  
		Last Modified: Wed, 12 Mar 2025 20:22:37 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
