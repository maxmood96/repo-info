## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:c88e4d0538faa2418ed2bdb3652dffbed85bab23bdf75a4ef5a7fc45afd8722c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.2159; amd64

```console
$ docker pull mongo@sha256:a3cf614ffba64c7789d442f60c03f0686199f3893f6d98c341a0034e84f5809c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366211554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7d01c567407dd4d26ba8db002e8ba1e237000e9ab913b0c1f72815ca89be51`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 02 Dec 2023 12:14:23 GMT
RUN Apply image 10.0.20348.2159
# Fri, 05 Jan 2024 00:48:26 GMT
SHELL [cmd /S /C]
# Fri, 05 Jan 2024 00:48:27 GMT
USER ContainerAdministrator
# Fri, 05 Jan 2024 00:48:40 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 05 Jan 2024 00:48:40 GMT
USER ContainerUser
# Fri, 05 Jan 2024 00:48:41 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Fri, 05 Jan 2024 00:48:42 GMT
ENV MONGO_VERSION=4.4.27
# Fri, 05 Jan 2024 00:48:58 GMT
COPY dir:9a4451ece440a57e287596f9b8b98884938e76dd62cf67441f8c60aeee0d3e41 in C:\mongodb 
# Fri, 05 Jan 2024 00:49:04 GMT
RUN mongo --version && mongod --version
# Fri, 05 Jan 2024 00:49:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 05 Jan 2024 00:49:05 GMT
EXPOSE 27017
# Fri, 05 Jan 2024 00:49:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:075332bb10f7fc70c56f7c073dd753e05cacbc93a38c181c5576739a29f8a7e1`  
		Last Modified: Tue, 12 Dec 2023 21:35:16 GMT  
		Size: 120.8 MB (120757041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0fc0c205aae21ed35899fd0fc23fff102859b9e5772bd5346f216befc7d29c`  
		Last Modified: Fri, 05 Jan 2024 00:49:13 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc38014092b92da663107ece5a3a4aefb3113f917abdf0482b3cb5debc1585e`  
		Last Modified: Fri, 05 Jan 2024 00:49:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2490cc6a48d1ad7ce3b38357dc0381977b4d83e67b597a7584ac6a15e5986c8f`  
		Last Modified: Fri, 05 Jan 2024 00:49:11 GMT  
		Size: 100.2 KB (100218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a278d3b12c5e28676dba2041b69b07f5d724037d9d221fe69a74fd99c131997b`  
		Last Modified: Fri, 05 Jan 2024 00:49:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ad90011513d8a4cfd5b5f126a2fd8637d0624a8951e7c8c02b00a91e396c4d`  
		Last Modified: Fri, 05 Jan 2024 00:49:11 GMT  
		Size: 263.4 KB (263383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786a8780e1e29be5178f72f06f8429648348f1d7968e417a07cf1f4bda59ccaf`  
		Last Modified: Fri, 05 Jan 2024 00:49:11 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ad6efd86e47711028e1ba42650094a4bbd8061a40497fcbc9f87a60ec1d4d5`  
		Last Modified: Fri, 05 Jan 2024 00:49:34 GMT  
		Size: 245.0 MB (244979282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9a1f97fb7b5f1076a198fff6baa28d85dfc0a4b7d243a75d93ae10b5d8cae`  
		Last Modified: Fri, 05 Jan 2024 00:49:09 GMT  
		Size: 104.4 KB (104355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf96b570dee0126000fdf557f8ffcae6aab49803c169349762860be188b9061`  
		Last Modified: Fri, 05 Jan 2024 00:49:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94800cff7e8926f806fc12f019c2369b7edb8997b0bbd0bb12466788fa7007`  
		Last Modified: Fri, 05 Jan 2024 00:49:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e9c79ea4c76174f9b669973077f9deeb04a01bb026ea5e846516b2b80a66f`  
		Last Modified: Fri, 05 Jan 2024 00:49:09 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:df177e806a35c334a234fe6cc355e573341b2810b85963e1d7b643cd2bd8e53e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 MB (349896607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aafe7469fef3eab84e28f54fdf72db9a12dab4bfd49726662054de64ca42036`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Fri, 05 Jan 2024 00:48:41 GMT
SHELL [cmd /S /C]
# Fri, 05 Jan 2024 00:48:43 GMT
USER ContainerAdministrator
# Fri, 05 Jan 2024 00:48:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 05 Jan 2024 00:48:55 GMT
USER ContainerUser
# Fri, 05 Jan 2024 00:48:56 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Fri, 05 Jan 2024 00:48:57 GMT
ENV MONGO_VERSION=4.4.27
# Fri, 05 Jan 2024 00:49:12 GMT
COPY dir:9a4451ece440a57e287596f9b8b98884938e76dd62cf67441f8c60aeee0d3e41 in C:\mongodb 
# Fri, 05 Jan 2024 00:49:19 GMT
RUN mongo --version && mongod --version
# Fri, 05 Jan 2024 00:49:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 05 Jan 2024 00:49:21 GMT
EXPOSE 27017
# Fri, 05 Jan 2024 00:49:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68491743f95cfd348a1e6ee6b743a0c2be61351dc9372ae5be4cd7f8b61034ea`  
		Last Modified: Fri, 05 Jan 2024 00:49:29 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90423d088b168f9504a9a64469573066e346592f5679fcd271c968ac75e5de8`  
		Last Modified: Fri, 05 Jan 2024 00:49:29 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8377a0bbe244b2bc9c9932546cc8d0b170b931c12f38f18e0a465ec49c8d0`  
		Last Modified: Fri, 05 Jan 2024 00:49:27 GMT  
		Size: 68.5 KB (68502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587795f19616f748f6f6bd5febfe8cc6206bbdbd8767b5ca5885ed0c57da6762`  
		Last Modified: Fri, 05 Jan 2024 00:49:27 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06c11c7aee8591bba81e1b08ee0c84ff44ec3367de8366657219e2605fb5e1b`  
		Last Modified: Fri, 05 Jan 2024 00:49:27 GMT  
		Size: 263.4 KB (263381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38728808607d0beac685349790294b4ec84a9ace39ce6aa85bf38bdb2a502f7`  
		Last Modified: Fri, 05 Jan 2024 00:49:27 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1043391eedf711f4ff658e59a950da02a91889c88bcf28584341ae7ce1448047`  
		Last Modified: Fri, 05 Jan 2024 00:49:50 GMT  
		Size: 245.0 MB (244979323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53401b75f8a7311e246dbafcedaa6aefdf0b02273bb3cc2164e663a0814695a4`  
		Last Modified: Fri, 05 Jan 2024 00:49:25 GMT  
		Size: 67.9 KB (67915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152f43a578062cefaef7f4a91e8ebd2e6f1077f0d18793c812afa28562b9cf1`  
		Last Modified: Fri, 05 Jan 2024 00:49:25 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d03dd802488f787ed1a8d33fca417702fef0d5c20801615b90ce2fcf87275`  
		Last Modified: Fri, 05 Jan 2024 00:49:25 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ce306e6b6a838a931cf981f5b07a921ed446341de66cf5ffae9e002a43d6e9`  
		Last Modified: Fri, 05 Jan 2024 00:49:25 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
