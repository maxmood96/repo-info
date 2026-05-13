## `caddy:2-nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:f36d647cd0abf69477f706805f4f432c5e46018df5889798b0ad2587f79c00e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `caddy:2-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull caddy@sha256:c3519d7305383d7d98fd5655f5b214c168bf143fac21373601d3256d95cdcb51
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217846345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27b31074e7aaff3dda62912ec8012a7c16966860e6b9706b3de621ab0eed09a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 12 May 2026 22:09:34 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 12 May 2026 22:09:36 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Tue, 12 May 2026 22:09:42 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 12 May 2026 22:09:46 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 12 May 2026 22:09:47 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 22:09:48 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 22:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 22:09:49 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 22:09:49 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 22:09:50 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 22:09:50 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 22:09:51 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 22:09:51 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 22:09:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 22:09:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 May 2026 22:09:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 12 May 2026 22:09:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 12 May 2026 22:09:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 12 May 2026 22:09:57 GMT
RUN caddy version
# Tue, 12 May 2026 22:09:57 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5512968fadbbf784e0ca5cc589acd26cbbfd7682242072ca8e721c19b622816`  
		Last Modified: Tue, 12 May 2026 22:10:07 GMT  
		Size: 78.2 KB (78157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40221bc2bec8b874e44fe2430a1869ed16ee2dbeebdbba006a0653e51df0924a`  
		Last Modified: Tue, 12 May 2026 22:10:10 GMT  
		Size: 17.5 MB (17549651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807b7f3ddf8b5be295671800b9dc5aa5b3574c8e75fe375f6022edf78a21ed50`  
		Last Modified: Tue, 12 May 2026 22:10:07 GMT  
		Size: 264.7 KB (264693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a7f72f234d9f3936301bbb9b9d67ef56048e9cf171a67117d56de6e21c44e`  
		Last Modified: Tue, 12 May 2026 22:10:07 GMT  
		Size: 110.4 KB (110401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d338c6f02fb8409c8b0161c594ebdbd39456c1cb217fe49e5bddac55648e5c`  
		Last Modified: Tue, 12 May 2026 22:10:06 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31db57711163416d36f5683d956aed991eae03968434c11b24b9644a7d28c563`  
		Last Modified: Tue, 12 May 2026 22:10:05 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503570c62716ff282cc3af334a82afdcb1b8d65f13ddc6888fe9af11dc339bcd`  
		Last Modified: Tue, 12 May 2026 22:10:05 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d25f0053c0ea3796d13e364ca108a845fd8254c27e82f596e872898e92d50e`  
		Last Modified: Tue, 12 May 2026 22:10:05 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c440a6b55e26c75827452a0d350028e1b636d5fd104fcf4bfdb94b062b29729`  
		Last Modified: Tue, 12 May 2026 22:10:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d45a52e656c0620cdae22bad90758ed168cab036f7f98166f4fcfa899b42e74`  
		Last Modified: Tue, 12 May 2026 22:10:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c99947e74781144e4c150051dc69ea21cc9e3b54066a0cfd64173c92659e7`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f1e2ec676acc60b2935c0af8383a385bf1dfbddb6991457448a124eb51ed13`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba7944fe6a0b091bbe5aa4545c6093e4c8b36b17be369b8d1b6bac7a50bfec4`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8c2734586b07c8373256f5a4714f7a749195c25c086e4c8d2c55867c47e9b9`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abddf227655952662fa1d5531a04c0a52dafce507e64fc1d6ada050fd8552f2e`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f75985f41ec2531e80784f83cc48df1a3d1547443ffe9c840f33ecd9c6c5ad`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7dd6f85c4cd1829d6e5237aaf7360d25597997f9799fcd3d0852775924db9c`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511522136fc9a6bb055e6a3f82b4f30d4fef0c9cd8efde616579c11955b490fc`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f664641ae2d2f16975ab40c9fa435fa91f664dd81a15d9d0a2bb69e2ff0ccbe8`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 110.4 KB (110393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc4c31270e45e042b5753f312d4184a4160d556108d96df9494a13ff2acf941`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
