## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:062e5dc64ae073bdaafd9cc8029bb97d9e9f062a68f6cd3b2703f6547924c9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:29cd8b92ab07e93285ec1840400d244b05d6638c57207e28ffc26533712c089e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.0 MB (466957915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583ecac2646dfa658c248db50b3377a68c16b04bfdd866500c59c6be2bebdda5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 23:57:31 GMT
SHELL [cmd /S /C]
# Wed, 09 Oct 2024 23:57:32 GMT
USER ContainerAdministrator
# Wed, 09 Oct 2024 23:57:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Oct 2024 23:57:35 GMT
USER ContainerUser
# Wed, 09 Oct 2024 23:57:36 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Wed, 09 Oct 2024 23:57:37 GMT
ENV MONGO_VERSION=5.0.29
# Wed, 09 Oct 2024 23:57:54 GMT
COPY dir:2a264fe791bba3a77954956eed4741f2ec3b2e15bd00a3c81924c3459cafe2f1 in C:\mongodb 
# Wed, 09 Oct 2024 23:57:58 GMT
RUN mongo --version && mongod --version
# Wed, 09 Oct 2024 23:57:59 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Oct 2024 23:58:00 GMT
EXPOSE 27017
# Wed, 09 Oct 2024 23:58:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ec1a5c8e36d764260d04452d4185cac411e225ae3a37a73cd67543526feb59`  
		Last Modified: Wed, 09 Oct 2024 23:58:09 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bee205e2bdb156d200e99aedbf7d8885355fb71b9937921a2daa5bbabfbb36`  
		Last Modified: Wed, 09 Oct 2024 23:58:08 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c732ba37c902750f24a6915f64027b729d6edf3630c179617b877a1509bb5b`  
		Last Modified: Wed, 09 Oct 2024 23:58:07 GMT  
		Size: 71.7 KB (71719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c60394f4657cc162ec9273be486bf650c536fabbd7307e81febb2b91ef73ee`  
		Last Modified: Wed, 09 Oct 2024 23:58:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47c5bf45de95400b34108848be1182ba58bcbadd3524e50a3942c4108352719`  
		Last Modified: Wed, 09 Oct 2024 23:58:07 GMT  
		Size: 275.4 KB (275358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9e067c8ecbf064ecb0fd120333125e072fd9e44585ae14d002d8d0e0ae8bcb`  
		Last Modified: Wed, 09 Oct 2024 23:58:07 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a9341095ef919e20b09f03195e07bfa5df5e8e328cca040d540652f3a82525`  
		Last Modified: Wed, 09 Oct 2024 23:58:34 GMT  
		Size: 311.4 MB (311423133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2617af4691e7756875ba03fedb3b77be83fb2ce4ef602c28a40687241137808`  
		Last Modified: Wed, 09 Oct 2024 23:58:05 GMT  
		Size: 86.9 KB (86857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1acaf4f34d795c8e675c0f1ffe876c508d707409777880c7117a057c5bba1e`  
		Last Modified: Wed, 09 Oct 2024 23:58:05 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87308b17686c8a587fd1c28dece9ed5773b680e36a4466362bddbdb14086f323`  
		Last Modified: Wed, 09 Oct 2024 23:58:05 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c5d73a2363a0a33cc750ee05f503512ec5413e1be51fdd7f30a49269d4548d`  
		Last Modified: Wed, 09 Oct 2024 23:58:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
