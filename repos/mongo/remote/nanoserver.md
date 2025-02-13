## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:e8d1ddb08a45539b0e2ab3e536ab1c43d93421b0d3ad88112b9c1376a2ec7271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `mongo:nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:6b09be3647f2132ef45f5ebc32dd6b36582e38ff62c097bbfc556b392e6d8ba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **888.7 MB (888721449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01574fe5e5c7c3aeca36a2959c6d996a8d20930a48e386160350830343c7e3a2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:20:06 GMT
SHELL [cmd /S /C]
# Thu, 13 Feb 2025 01:20:06 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:20:09 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 13 Feb 2025 01:20:09 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:20:11 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 13 Feb 2025 01:20:11 GMT
ENV MONGO_VERSION=8.0.4
# Thu, 13 Feb 2025 01:20:39 GMT
COPY dir:0009924507cd67bb774ae279cf5a575db39e491af9c3c9f55c5a3622f7b63de5 in C:\mongodb 
# Thu, 13 Feb 2025 01:21:00 GMT
RUN mongod --version
# Thu, 13 Feb 2025 01:21:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 01:21:01 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 01:21:02 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af24ab82ad99f33425e2411d9aaab878fc56fedf3c03cca15700b57fe56a82a`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a13123a880be31c5a5afcbfc8dc38aa746613bfbe7921155af7f2d6ac189e66`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d574986d20a22b3592556b7e3aecdb637cd2ec743923789c3dbb851bd3277a`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 76.0 KB (75965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a25fa4a4a1ed71416a9d6a3a7ae6026503afee6e7b907cd942078f5a4d4069b`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a562bfb26cd222234ee83ed4b2311a380b20d4d49c283215753091d22d6842`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 275.2 KB (275154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463c253d057d61a2ce66d542e4294c842b8a99a257f2c9aa8ebde20963eae60`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7ff4135d8795af8f38e9ed128637a6c6a8a50ba2281679646857cb50eec5ec`  
		Last Modified: Thu, 13 Feb 2025 05:15:15 GMT  
		Size: 767.6 MB (767598473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9de5f7fb8b96839d9e5a872f5ab76d9edba625b58557b2fab408e702d2bfdb`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 98.0 KB (97998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e04eb269455612961f05b2f5c0a2cfec48868dda0a6e9524a64feb25fa6dc57`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7c4fd60305352177c07cffb10f1cbb10b9689bb1cabe551fba087b4088f731`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7705e4962c5eb09fc08056c523b198e4062769c39f48b3f8bc1e27289ded3521`  
		Last Modified: Thu, 13 Feb 2025 05:08:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.6893; amd64

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
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec58fdf3bc8a2b07cd3b80f3b0949d6046a406498c328951ab9368c3ee36906`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258353adf0ad61e57cd50f92c654042ba6d4c5ea3e849e0d1678c9cab782f6d7`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91eecf065186b708e84843fda20ce024b65c7f0b50f8368e7e14b469288d6da`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 72.1 KB (72098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4a1b014d2b1e352d87e8b14dfef5fdf4ac6a2f5566bceef0062edef5774f9e`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994a173fe81b716d76fb7a2c8bbf2508c4b0af57ecb23e6d4df3d09dd4a97c00`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 275.2 KB (275168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa91a743c3d0598e98f49e0e0b470af055d3bf2498f160ceac1fb43b00a03ab2`  
		Last Modified: Thu, 13 Feb 2025 05:08:24 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e7dc46a6c4b83a50805ecdaaaca6ebe6852fd0a50039e5c268c0baa21d9a0`  
		Last Modified: Thu, 13 Feb 2025 05:08:45 GMT  
		Size: 767.6 MB (767598564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b258bb1304b96433046272ee72c1aa584aca235b924239322cabca61cfdadd0`  
		Last Modified: Thu, 13 Feb 2025 05:08:25 GMT  
		Size: 86.4 KB (86382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8281eb51081a3a4fa2943b69117a90da9a72bed86cd3d0dccf104aa7edfea5`  
		Last Modified: Thu, 13 Feb 2025 05:08:25 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c43670895a15b1d77bf211849d6ebaef59210374f139477540d963f88944c0f`  
		Last Modified: Thu, 13 Feb 2025 05:08:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d61584ee0c08214d66688e450023850a83f65ed1fad1d8d26cdb51d892b653`  
		Last Modified: Thu, 13 Feb 2025 05:08:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
