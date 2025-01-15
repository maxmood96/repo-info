## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:4b6605c4baa4fdfe9f6bbc34a1c288ef8cdf7b08fa66a76d8fe0fa04f7dff2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull mongo@sha256:982d9d9449e8fdb3018d54c5e75f06b4eda74c0ea905e61d5c6d737ad9d46bc0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.8 MB (646797152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3792d68ba7200d65e0fd8272e0e82505475f862078116812a06e7212114d870c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:04:03 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:04:03 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:04:06 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jan 2025 18:04:07 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:04:08 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Wed, 15 Jan 2025 18:04:08 GMT
ENV MONGO_VERSION=6.0.19
# Wed, 15 Jan 2025 18:04:26 GMT
COPY dir:f97029ff7a52e12f6b8e5522b58ebccd35083615a35a3126b84db5898f526c7b in C:\mongodb 
# Wed, 15 Jan 2025 18:04:40 GMT
RUN mongod --version
# Wed, 15 Jan 2025 18:04:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jan 2025 18:04:42 GMT
EXPOSE 27017
# Wed, 15 Jan 2025 18:04:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a0b1e5d10e84d435db23d5bda1e3a5e023155f2b0626a1ec5cdbd1df765461`  
		Last Modified: Wed, 15 Jan 2025 18:04:47 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f5f6061851088b5cd0bc86e72932f4ccc557007e5f94e031c311767deb7056`  
		Last Modified: Wed, 15 Jan 2025 18:04:47 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d72c05c51af54c0c08155d336666b4a75c83431003cb5d99376570075a43`  
		Last Modified: Wed, 15 Jan 2025 18:04:46 GMT  
		Size: 78.8 KB (78762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86354dfc09d30da8c8bd7c1001cdca29d97c0b4d531d06a82638e8246fcb327`  
		Last Modified: Wed, 15 Jan 2025 18:04:46 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6215a2e67358c08d94d1ae634789985551bda0ca8d63065672f17e0cb0751650`  
		Last Modified: Wed, 15 Jan 2025 18:04:46 GMT  
		Size: 275.1 KB (275144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246fdbc1c0954bb01abc5cbba133d33ea16cd6b111540b94f68db938e2fb2996`  
		Last Modified: Wed, 15 Jan 2025 18:04:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329fafeefea247e045184c40b91bca6147afcb0ef487f2edc9dc86633b2a3f01`  
		Last Modified: Wed, 15 Jan 2025 18:05:26 GMT  
		Size: 525.7 MB (525677051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f57f26b2c2520dfaac4bb87368b5776016559c8380dd009602a4658ce3a52b`  
		Last Modified: Wed, 15 Jan 2025 18:04:45 GMT  
		Size: 97.4 KB (97427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2009217b1cd7421c9cb8fd07da6f369679025809aa8ca0fcdf9e692c1d44e9a4`  
		Last Modified: Wed, 15 Jan 2025 18:04:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90c2069af097d0687a9c3cd9f27f12a2de7516676625c1b6485f7b67b5ef687`  
		Last Modified: Wed, 15 Jan 2025 18:04:45 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702af774deeb060862b68412bfb4eb77b308e991712a9906591f536f004a2c09`  
		Last Modified: Wed, 15 Jan 2025 18:04:45 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
