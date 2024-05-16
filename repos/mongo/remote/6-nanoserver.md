## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:63bb027f41188c2c4984c9a82767d9f5826d429128894c4f7787574daf2e0669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:73d82bb148eb1e6b69c47d271d1127ef9eb3bb7a4e9f759726add3b2c17bdad4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.2 MB (637203226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf7a0627d35ae2085ca38c22d7d8fdea12436f9fbfd25f39f25b91eb619c45`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 22:52:49 GMT
SHELL [cmd /S /C]
# Wed, 15 May 2024 22:52:49 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 22:53:19 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 May 2024 22:53:19 GMT
USER ContainerUser
# Wed, 15 May 2024 22:53:21 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 15 May 2024 22:53:22 GMT
ENV MONGO_VERSION=6.0.15
# Wed, 15 May 2024 22:53:42 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Wed, 15 May 2024 22:53:55 GMT
RUN mongod --version
# Wed, 15 May 2024 22:53:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 22:53:56 GMT
EXPOSE 27017
# Wed, 15 May 2024 22:53:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f011f3a265d8b50d3aee5d0f99b216199b59e78c7dcd3c9d6caedf33d2dc41f`  
		Last Modified: Wed, 15 May 2024 22:54:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f21f9f5567148257130c5666c7afba341fa6b9d628d5d87c00e271f67079731`  
		Last Modified: Wed, 15 May 2024 22:54:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8762e0b353ea678ecda06c0e3f79412639bbe26a8a7c39e5ce55ad9ac08942`  
		Last Modified: Wed, 15 May 2024 22:54:01 GMT  
		Size: 86.0 KB (85973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0e1a0030fca7e8fef8890709c1fe24537d08650925e66977e8ad1cc2eca0f0`  
		Last Modified: Wed, 15 May 2024 22:54:00 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0ece0045bc0efeff7388123c68cc5de1b737db8a9825ee9fd8bb5a2d605d12`  
		Last Modified: Wed, 15 May 2024 22:54:01 GMT  
		Size: 267.1 KB (267069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8722db442e660d3225110284069d11e8195072251bd5676143b07dad01176c6f`  
		Last Modified: Wed, 15 May 2024 22:54:00 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b5defb0f237406410510eb1707499a4ae5ec271585afbe561012906a22221e`  
		Last Modified: Wed, 15 May 2024 22:54:41 GMT  
		Size: 516.3 MB (516321149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3da5797fc2887f205755f9b0d8848967df6c141b88724d519a08976e99ae53e`  
		Last Modified: Wed, 15 May 2024 22:53:59 GMT  
		Size: 96.3 KB (96299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f0575a5bd0e72d3a0be84441cd8a122a87589766010af26b3847eed0972d9`  
		Last Modified: Wed, 15 May 2024 22:53:59 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b837c26ae87b2f8359d6e8a02e4e2e660bb730a82f4d8b8708eb1025e41330fd`  
		Last Modified: Wed, 15 May 2024 22:53:59 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fabeee4e3330bf7358580e6a01605b7e6a00b129b22290820c3304a57103926`  
		Last Modified: Wed, 15 May 2024 22:53:59 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull mongo@sha256:f5ff4d6a7543dd46680199519da787ac0d58bbdfda0af5831d4c031cfdf4f84a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672780842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41279ee161de1124645b83ee7318ac01a3f8793ed08e680ab07362001464c648`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 22:52:34 GMT
SHELL [cmd /S /C]
# Wed, 15 May 2024 22:52:35 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 22:52:42 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 May 2024 22:52:42 GMT
USER ContainerUser
# Wed, 15 May 2024 22:52:43 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 15 May 2024 22:52:44 GMT
ENV MONGO_VERSION=6.0.15
# Wed, 15 May 2024 22:53:16 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Wed, 15 May 2024 22:53:29 GMT
RUN mongod --version
# Wed, 15 May 2024 22:53:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 22:53:29 GMT
EXPOSE 27017
# Wed, 15 May 2024 22:53:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcd7b3ccfb8926f2756ee8257d2f0d5df4d8206f941262e524279007ea4a44a`  
		Last Modified: Wed, 15 May 2024 22:53:36 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57f7a312abbb671d3220a693fc55fb76855e906d7366fc9986556bf6933dd`  
		Last Modified: Wed, 15 May 2024 22:53:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5f530e61a66275837c64a5379fe43de7c4dce7a9be85545cd1a569c60aa952`  
		Last Modified: Wed, 15 May 2024 22:53:36 GMT  
		Size: 66.6 KB (66607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c827d662aa7affd28096f7e8bf5e0c65f805871dfbf30ddcb377bbcdaeeb36f1`  
		Last Modified: Wed, 15 May 2024 22:53:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b80a0a50e0da62e14c0a7a053abdd453670c8b3b7cc75976e7ee0261e98f7a`  
		Last Modified: Wed, 15 May 2024 22:53:35 GMT  
		Size: 267.1 KB (267058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a4fe28e5de20595f391f8c18594be8fa26f1f5ed3e6ecc9c0ced447bf3692b`  
		Last Modified: Wed, 15 May 2024 22:53:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db34a4f20ec8d2c3253716f771de24bf6098080015ecf921745e634ad44cd7b9`  
		Last Modified: Wed, 15 May 2024 22:54:16 GMT  
		Size: 516.3 MB (516321160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9415e52e20552a18eb08928408b2527b21d0c67fe5338890e5eb0747c0291e48`  
		Last Modified: Wed, 15 May 2024 22:53:33 GMT  
		Size: 1.2 MB (1177389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41d655db1c5af290cf8084815b2020a220631918cd387a92058512ad9a01f9a`  
		Last Modified: Wed, 15 May 2024 22:53:33 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa59da49fc3703ffa66a31953e98747edb65b11553cbd3da6f903bdad366087`  
		Last Modified: Wed, 15 May 2024 22:53:33 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa79d6f321e3d4605553f0cb502450ef4322372fe05804e3298a8d324f20d49`  
		Last Modified: Wed, 15 May 2024 22:53:33 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
