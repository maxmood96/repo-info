## `caddy:nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:73c6b34a841c78bd89f5c191dcc0c93ed655881e3134962ca4164ea7946d6256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `caddy:nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull caddy@sha256:81e72c61c291c04f95e718e7272c948362ee670bd675312db77afa6401e42a12
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143064334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ee039c63882485e963f94253193318c71ec85119c305112df09fd57390ae02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Mon, 08 Dec 2025 18:36:36 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Mon, 08 Dec 2025 18:36:40 GMT
RUN cmd /S /C #(nop) COPY file:32cf40eadbbb089db5d2a89aab3783b917db3d218ef99bdd6915c6b4af650c32 in c:\caddy.exe 
# Mon, 08 Dec 2025 18:36:45 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Mon, 08 Dec 2025 18:36:48 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Mon, 08 Dec 2025 18:36:49 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Mon, 08 Dec 2025 18:36:50 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Mon, 08 Dec 2025 18:36:51 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.10.2
# Mon, 08 Dec 2025 18:36:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Mon, 08 Dec 2025 18:36:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 08 Dec 2025 18:36:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 08 Dec 2025 18:36:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 08 Dec 2025 18:36:54 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 08 Dec 2025 18:36:55 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 08 Dec 2025 18:36:56 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 08 Dec 2025 18:36:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 08 Dec 2025 18:36:57 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Mon, 08 Dec 2025 18:36:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Mon, 08 Dec 2025 18:36:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Mon, 08 Dec 2025 18:37:06 GMT
RUN caddy version
# Mon, 08 Dec 2025 18:37:07 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a071a64f08d241cb2a88fe51d0b21b994a0bbcc02ba7b003bbac1c4d4dd51e2`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 72.0 KB (72008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b962d7b112367ae7e987f363f6f7f3de246fffc61003a4078cadb739d6413fc4`  
		Last Modified: Mon, 08 Dec 2025 18:37:48 GMT  
		Size: 16.2 MB (16217706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce41ee91d9731a579ddbf8b4999b2a7b37a754429dd2c22bb0935b84dfc6597`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 157.2 KB (157161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb6b95b00e82b2351eff813c85c0ba6d2d6dc5ddcf86eff813d357d93310e5f`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 124.4 KB (124381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96590d0b62b057b940c883ad1f1693729b11a2b5d003762a449eca4841cd73b4`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57695fbd0115b3b97e48017cb048b72ed26b38bc39ac08a1bccd56edf4aabcb2`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eb5ef3250411be07d35f83638f9ba54591056d585fd070d5ff8a1557cf59a8`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2fb6454486899ed837b523908861cb6387f995df17b5d4033c042aab89cca`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874f8b4f333f878a495787e5ece7c4f27691c11122ccebd22b31be793e2f2a1f`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83dbde2728d20972341a052e576a0bcb6fddc3c7ad993a28c12f7d19fd745bd`  
		Last Modified: Mon, 08 Dec 2025 18:37:47 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af523d37ddcdd58617c90a19469d21d4fbefd831df9aefd7fd5011d4144b31a`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83d584d87e5bd396158956725f754112989f088e39a3038926bfbaf3ab79e88`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810876dbd58d6c2948b43f2c84fbeafcd258ad89e7cc59cf263e323dc37dff93`  
		Last Modified: Mon, 08 Dec 2025 18:37:47 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e229ab2781671a64795fdd537e76f280d3c2746930a231887b7dfd683f6ae936`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f238ead98d0879d6589fa7dcacf316114ee9ab4b2e81d79c8a8727d2f2f1cb`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f790a1ed705f6eb8300ed90718ac3a7c1adcb8290dfa8fbcdd96a3ca622f4e1`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cb954fd54aa8dc260dffcfe09a96308efa139047c115b0044da19c33c555fa`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75827b361987b28aeb2db502b024ed692cbae88e0bb8148d4904cc3ba0f021f8`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45db563bd5eceeea17d4c9ca2c08cf3ffc7c71cd69ec51e35347e69846f6fcac`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 128.2 KB (128210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c3316cd00a59c073c844cc90d7de8c12f28a8c2854c78bde69c8e2e3c280cf`  
		Last Modified: Mon, 08 Dec 2025 18:37:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
