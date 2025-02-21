## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:32e3b013f02caa0f6f26e4fa9511ef91f5eccf5405dfc939c7195dbdaa9b4184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull mongo@sha256:9d303b270094b67bac5f3d796292d672e7216f4c6fa43308f2e9dc1ab32aa1ca
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.0 MB (874954963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84265e3a6d40a75529392957b252f6aad819ccd56cb894786d9619ff638b687a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:17:19 GMT
SHELL [cmd /S /C]
# Thu, 13 Feb 2025 01:17:20 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 13 Feb 2025 01:17:23 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:17:25 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 13 Feb 2025 01:17:26 GMT
ENV MONGO_VERSION=8.0.4
# Thu, 13 Feb 2025 01:18:09 GMT
COPY dir:0009924507cd67bb774ae279cf5a575db39e491af9c3c9f55c5a3622f7b63de5 in C:\mongodb 
# Thu, 13 Feb 2025 01:18:26 GMT
RUN mongod --version
# Thu, 13 Feb 2025 01:18:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 01:18:27 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 01:18:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec58fdf3bc8a2b07cd3b80f3b0949d6046a406498c328951ab9368c3ee36906`  
		Last Modified: Thu, 13 Feb 2025 01:18:32 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258353adf0ad61e57cd50f92c654042ba6d4c5ea3e849e0d1678c9cab782f6d7`  
		Last Modified: Thu, 13 Feb 2025 01:18:32 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91eecf065186b708e84843fda20ce024b65c7f0b50f8368e7e14b469288d6da`  
		Last Modified: Thu, 13 Feb 2025 01:18:32 GMT  
		Size: 72.1 KB (72098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4a1b014d2b1e352d87e8b14dfef5fdf4ac6a2f5566bceef0062edef5774f9e`  
		Last Modified: Thu, 13 Feb 2025 01:18:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994a173fe81b716d76fb7a2c8bbf2508c4b0af57ecb23e6d4df3d09dd4a97c00`  
		Last Modified: Thu, 13 Feb 2025 01:18:31 GMT  
		Size: 275.2 KB (275168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa91a743c3d0598e98f49e0e0b470af055d3bf2498f160ceac1fb43b00a03ab2`  
		Last Modified: Thu, 13 Feb 2025 01:18:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e7dc46a6c4b83a50805ecdaaaca6ebe6852fd0a50039e5c268c0baa21d9a0`  
		Last Modified: Thu, 13 Feb 2025 01:19:29 GMT  
		Size: 767.6 MB (767598564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b258bb1304b96433046272ee72c1aa584aca235b924239322cabca61cfdadd0`  
		Last Modified: Thu, 13 Feb 2025 01:18:30 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8281eb51081a3a4fa2943b69117a90da9a72bed86cd3d0dccf104aa7edfea5`  
		Last Modified: Thu, 13 Feb 2025 01:18:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c43670895a15b1d77bf211849d6ebaef59210374f139477540d963f88944c0f`  
		Last Modified: Thu, 13 Feb 2025 01:18:30 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d61584ee0c08214d66688e450023850a83f65ed1fad1d8d26cdb51d892b653`  
		Last Modified: Thu, 13 Feb 2025 01:18:30 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
