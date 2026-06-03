## `caddy:nanoserver`

```console
$ docker pull caddy@sha256:8106df599a3a6139cc8076f902fa6392a0771091a978edcb78b52b97d908debf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:nanoserver` - windows version 10.0.26100.32860; amd64

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

### `caddy:nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:3c0ef5c5c68ca76d04da39c4388fcc945f4a0226bf0d91aa402e8ade9df765c8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145293716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e19c6f0c931a9e4114315cba5e4479702a5137d9d074b0c8d66470fb91c40c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 03 Jun 2026 19:14:07 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 03 Jun 2026 19:14:23 GMT
RUN cmd /S /C #(nop) COPY file:7d2f419889d1c745e8d01a18ec688d43a6c8f6363f61c1964c7e88fd70b1b987 in c:\caddy.exe 
# Wed, 03 Jun 2026 19:14:32 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 03 Jun 2026 19:14:37 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 03 Jun 2026 19:14:38 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 03 Jun 2026 19:14:40 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 03 Jun 2026 19:14:41 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.4
# Wed, 03 Jun 2026 19:14:43 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 03 Jun 2026 19:14:44 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 03 Jun 2026 19:14:45 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 03 Jun 2026 19:14:47 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 03 Jun 2026 19:14:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 03 Jun 2026 19:14:49 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 03 Jun 2026 19:14:50 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 03 Jun 2026 19:14:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 03 Jun 2026 19:14:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 03 Jun 2026 19:14:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 03 Jun 2026 19:14:55 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 03 Jun 2026 19:15:06 GMT
RUN caddy version
# Wed, 03 Jun 2026 19:15:07 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e03ed2dd2bb83650ea7d03c4c542bed7a04d87bbc6fe62190ec805a7cbe9804`  
		Last Modified: Wed, 03 Jun 2026 19:15:17 GMT  
		Size: 71.3 KB (71335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bd91d1c25b7cb8e1db27fca64e8c9809d08526ba1794ab09a6c37e0fddba91`  
		Last Modified: Wed, 03 Jun 2026 19:15:19 GMT  
		Size: 17.6 MB (17619904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4e6eebf9e74b48c33d8d2f99133f2b37f21aafce70c2a91d9022658823d581`  
		Last Modified: Wed, 03 Jun 2026 19:15:17 GMT  
		Size: 290.6 KB (290602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a76c40fb84d41dfe1caf526aa72b38b771aefc2f24728ba2bcf9d956db2445`  
		Last Modified: Wed, 03 Jun 2026 19:15:17 GMT  
		Size: 129.0 KB (129036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776f38d4d4f4d7c5b0a5a210fa203e2b57bb8a94e11faa246cee24b50242feb4`  
		Last Modified: Wed, 03 Jun 2026 19:15:16 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8cf60573d31c756f25b8c8fa06fc5c2ef9401e3633a35f02713a14976a4090`  
		Last Modified: Wed, 03 Jun 2026 19:15:15 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993600e3b82c2a7a1e9f0b8ebdbf2fde846dc7df0d3ed9fb0e209593d35de1c5`  
		Last Modified: Wed, 03 Jun 2026 19:15:15 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95d6c7b18126ed9c452223b73dd09181f1e3e0855de9330615957e1e042be13`  
		Last Modified: Wed, 03 Jun 2026 19:15:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0aec4d95625b48f32122f48a3cf533729b96d656f9165f409ccf8edf93c135`  
		Last Modified: Wed, 03 Jun 2026 19:15:15 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bf4f3e53b2ba952fb32d10c3ad9ddf5a776edcc7c310ae3fe3a84205568182`  
		Last Modified: Wed, 03 Jun 2026 19:15:15 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c949fce248bb0c917e74e59b45b77b20db23b9bb800891f2beaf2fb9b7581679`  
		Last Modified: Wed, 03 Jun 2026 19:15:13 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6914c16a1d5813ec30dcdb28f54c864578959fca136d6dc432fe46a164a71de5`  
		Last Modified: Wed, 03 Jun 2026 19:15:13 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb7c16526f4bc8721f2b554bdf0c97f71ab5075a40f031e01d23b6078c819e1`  
		Last Modified: Wed, 03 Jun 2026 19:15:13 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43a3eb05a944aeb7aca5dba59e851b4f651822ae5c025ea297afee69e8fb6c4`  
		Last Modified: Wed, 03 Jun 2026 19:15:13 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8afd2cb77c9ea907630a35a47b633809a951da0f876697b90adad815f5cd1dc`  
		Last Modified: Wed, 03 Jun 2026 19:15:13 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703b8278392f7f62c4ecbfe8499368552423feb01b0e9fff1f7dc546f6949f5b`  
		Last Modified: Wed, 03 Jun 2026 19:15:11 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b1d910e7897d10e139b7dbb2c5d343ec775e12afffb49e501d30418dd950b2`  
		Last Modified: Wed, 03 Jun 2026 19:15:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b16efcc81628508d5ca281de28aea122ebbd1d2b53f1a1ea484fa79f69631`  
		Last Modified: Wed, 03 Jun 2026 19:15:11 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae10782720e4f4a2223e02a210a2bdecdf9acbaf094e51cf64ce9d500c343b7`  
		Last Modified: Wed, 03 Jun 2026 19:15:11 GMT  
		Size: 128.2 KB (128198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8181db4e142a954ec9854319bc352d629b0a7b20977347025069f66b197abc37`  
		Last Modified: Wed, 03 Jun 2026 19:15:11 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
