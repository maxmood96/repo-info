## `caddy:nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:aaff69da5bf90c38ef954c43d9e4209366f2a4fe5c509a9a94bfa801e00a65ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:2edf2df3200a2b43eaa9d435d4c099746bbc0ba60e41961da1315b370d075ae7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217949921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce2aa994cde9f034b855ddbee18098917fe4d246b16e38289826068d20f9acd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 03 Jun 2026 19:14:24 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 03 Jun 2026 19:14:37 GMT
RUN cmd /S /C #(nop) COPY file:7d2f419889d1c745e8d01a18ec688d43a6c8f6363f61c1964c7e88fd70b1b987 in c:\caddy.exe 
# Wed, 03 Jun 2026 19:14:46 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 03 Jun 2026 19:14:49 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 03 Jun 2026 19:14:49 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 03 Jun 2026 19:14:50 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 03 Jun 2026 19:14:51 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.4
# Wed, 03 Jun 2026 19:14:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 03 Jun 2026 19:14:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 03 Jun 2026 19:14:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 03 Jun 2026 19:14:54 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 03 Jun 2026 19:14:55 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 03 Jun 2026 19:14:55 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 03 Jun 2026 19:14:56 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 03 Jun 2026 19:14:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 03 Jun 2026 19:14:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 03 Jun 2026 19:15:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 03 Jun 2026 19:15:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 03 Jun 2026 19:15:15 GMT
RUN caddy version
# Wed, 03 Jun 2026 19:15:16 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3814c35de9eab021a6359893b85547d6874403eaae5d7f8d291f8a4871735ac`  
		Last Modified: Wed, 03 Jun 2026 19:15:26 GMT  
		Size: 70.9 KB (70876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365b3e3123e121cdde532c39e2e1f7e8e109dff2c31bb6c14965d2411f99e51f`  
		Last Modified: Wed, 03 Jun 2026 19:15:28 GMT  
		Size: 17.6 MB (17619904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e98b2363b1972a81907d4861b5cca81406f6e68098cee11efbe140edfc15e3`  
		Last Modified: Wed, 03 Jun 2026 19:15:25 GMT  
		Size: 270.4 KB (270449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbbc961a78cde3499f7484d6530344756c1eb2d005e9d5c4b67797a86027b05`  
		Last Modified: Wed, 03 Jun 2026 19:15:25 GMT  
		Size: 110.1 KB (110053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74784936726c7d203d1f191ba04157addda6a202b8bf89c82d6b47217d0d6048`  
		Last Modified: Wed, 03 Jun 2026 19:15:25 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe80e393760f5082525eeb8ae0cb269ab7191d4d722949104d4cc59778a2857b`  
		Last Modified: Wed, 03 Jun 2026 19:15:24 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de40dd5bd4cfc2cd1efa11e800d4fea49cd250cc2855369085d0262c16fe52a6`  
		Last Modified: Wed, 03 Jun 2026 19:15:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d13ba15552dbccacbb36065d28def4f2a2abac04134e9efb6ba06a600f6e9e`  
		Last Modified: Wed, 03 Jun 2026 19:15:24 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bcd5f446d8d3d1ad4f861c24a3bec870f2659ed780ffd514915704ff12deca`  
		Last Modified: Wed, 03 Jun 2026 19:15:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907fff9bac8cfc8ba7b050ea89572aa0b50ea869e47c4997c05bacc7e5403309`  
		Last Modified: Wed, 03 Jun 2026 19:15:23 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89124a4317e56de4dda291121d5c1e1659a461376ed1c39707fca7eb84339d94`  
		Last Modified: Wed, 03 Jun 2026 19:15:22 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cfe4404998eb7ff65565e2c8fc5031ecdf192fbbe65040da9616fd1c15121c`  
		Last Modified: Wed, 03 Jun 2026 19:15:22 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d2f74fb18a8dc61edc182457468b4d32b5eb775063e77daeba4a16f0be6cbc`  
		Last Modified: Wed, 03 Jun 2026 19:15:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a830048c8eb6e06312dc3e535b6bd73fd4ee7c44838c955b91a493ae93b92`  
		Last Modified: Wed, 03 Jun 2026 19:15:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f356df4d074671fd49c4edc83e842ad02d5ef5680b3f76ef71c9fe2419559cf6`  
		Last Modified: Wed, 03 Jun 2026 19:15:21 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d30e1b1ffcbd48209ff0f150821c91748d64bef0caf9c55d21088fb4aa77b6`  
		Last Modified: Wed, 03 Jun 2026 19:15:20 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af599b6bb5bc27d2f3a50637937dc33ef10164a9e3b68bf2277c7f32862c2c6f`  
		Last Modified: Wed, 03 Jun 2026 19:15:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f08fb67b13cbdb441b096082bf55de2d0c65177f793442fe2809f61380bc3c`  
		Last Modified: Wed, 03 Jun 2026 19:15:20 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d4499ce86aeb7433b6e5f0fc2560d4b847df1db625950ee3f4ae4dd7feebb0`  
		Last Modified: Wed, 03 Jun 2026 19:15:20 GMT  
		Size: 124.1 KB (124135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfebeff0125fc181a0667d453c43a1a722074cebb54ff9212c5ac7a57e38a13`  
		Last Modified: Wed, 03 Jun 2026 19:15:20 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
