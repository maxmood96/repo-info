## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:c84d73806463c468889dc2cf1b59112f385a3b3103c1659d80c9574ae3291ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull nats@sha256:d4e9d4ab43a801d3bca2f54fc7cdd461efaea77d73ce631918d4c7a917a7cb0f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113384315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b0c19eef1db175831d7c24ad80e6222efa1a1ec8c20b15c4237bc9ef53e4a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 02:22:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Apr 2025 02:22:27 GMT
RUN cmd /S /C #(nop) COPY file:eee3870bfbcd9bfddd3622d20a6c2075b583b61ab0944602ceefed02dee11aa2 in C:\nats-server.exe 
# Wed, 09 Apr 2025 02:22:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 09 Apr 2025 02:22:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Apr 2025 02:22:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Apr 2025 02:22:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8aedda5eefa464b3796031c9760dab7a2f11baf5c8f3873a6ef30f37f17821`  
		Last Modified: Wed, 09 Apr 2025 02:22:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce86d7310aeec229cfea893f2102af9c814f1a4f0183260e395452f16c7edb75`  
		Last Modified: Wed, 09 Apr 2025 02:22:32 GMT  
		Size: 6.5 MB (6455934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8921e64436c5526aa5450c9822ed85619dd4c7fcc94843d4dd3ea48dbebe4cc`  
		Last Modified: Wed, 09 Apr 2025 02:22:32 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1ed1b260ea2e394b7d3f8865ccdf0f15848c76fcdfed0fe3decc90e5299b7c`  
		Last Modified: Wed, 09 Apr 2025 02:22:32 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa33fe3760005a43bd874eb4f47ac48ef10be26d8b9874761ee67a52e7f296e1`  
		Last Modified: Wed, 09 Apr 2025 02:22:32 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be63e348f57c91b59412665c590591e73d7c5aa2e91e05325bde41aa32856c7b`  
		Last Modified: Wed, 09 Apr 2025 02:22:32 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
