## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:ac99e939a60c80ec10bb4b8eeffd44d0a7611920a4a0fac91b92aaa032e2bac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull mongo@sha256:1db1aab385cb019f046b29509eb6b98c064c6972bb76e919f84a5230b8f2c9f3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.2 MB (877221630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a46b44aa410eac19788dd903a495d406eb2263db29025442e3dd6d4d33acb3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 20:20:24 GMT
SHELL [cmd /S /C]
# Wed, 12 Mar 2025 20:20:26 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 20:20:27 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Mar 2025 20:20:28 GMT
USER ContainerUser
# Wed, 12 Mar 2025 20:20:29 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 12 Mar 2025 20:20:30 GMT
ENV MONGO_VERSION=8.0.5
# Wed, 12 Mar 2025 20:21:05 GMT
COPY dir:a57177c3820715e7790c25cd1624ad61fd2701fb2fd637d2847e81498bfa8394 in C:\mongodb 
# Wed, 12 Mar 2025 20:21:22 GMT
RUN mongod --version
# Wed, 12 Mar 2025 20:21:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 20:21:23 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 20:21:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64402bf31136a39dafd0e528c6ad8e2fcc9fe8bba8986a2c55831e8b0c36a84d`  
		Last Modified: Wed, 12 Mar 2025 20:21:28 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825930cedb886607d0c8cb07d7f7b406e02618fa5e24a7ee6b38956d25e781b3`  
		Last Modified: Wed, 12 Mar 2025 20:21:28 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc75bfb1be89e9625193cc4ccf02fba4e7fc259263763c6db3f8667b54c3dd0`  
		Last Modified: Wed, 12 Mar 2025 20:21:27 GMT  
		Size: 68.6 KB (68621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e826b6e65880bc58fd481e43c4b512c5ffadbe48afe3201f30923d9f871e5`  
		Last Modified: Wed, 12 Mar 2025 20:21:27 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39258df17c4b21af868df04f2173d1ec573bba39400a5f29d13cfcd9bc8a8c`  
		Last Modified: Wed, 12 Mar 2025 20:21:27 GMT  
		Size: 275.2 KB (275163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9a7b1e8abd8c28cee3c9e4ab7d888c8154fb8ed478d79abb9c94c1d67c1b59`  
		Last Modified: Wed, 12 Mar 2025 20:21:27 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fce69813ab2f8ae6ed9e8c4c8e872fc02952b1823f7ae61348e5e7f076042b`  
		Last Modified: Wed, 12 Mar 2025 20:22:24 GMT  
		Size: 769.9 MB (769890855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfdcf9e1be0f89a4f411a673df57be01955835933bf050ce5a8e804d0b60e56`  
		Last Modified: Wed, 12 Mar 2025 20:21:26 GMT  
		Size: 72.0 KB (71996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3db704f34aad58b788aaab76a4e85b21180dacdf1235d55f850258cd2dbb5e`  
		Last Modified: Wed, 12 Mar 2025 20:21:26 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271928fc510f018908db1f0aa40ec45abd0d35378d927d547c7ed2b6454a517`  
		Last Modified: Wed, 12 Mar 2025 20:21:26 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91c8a6df882dde95b06a7f9c47ca41d8a2dedbb7aea88466869c7b2bbfa1e2d`  
		Last Modified: Wed, 12 Mar 2025 20:21:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
