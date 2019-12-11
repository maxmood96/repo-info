## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:71bf025f0131d3ab0052913de0acda776986f6aa4af2308de0c9a2ec435fe7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull nats@sha256:5e8688d581549f9fede7d80271f22b3fd1e5ef20b2e6ca9bc5cbb275d079e39e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105099660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9e4279fd3cd1a4279984fe1770d85c2b0c9bd20ccb16327550d561e7119958`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:31:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 18:31:54 GMT
RUN cmd /S /C #(nop) COPY file:a9e3f6c9790c912d513d2134dc1f68e02a9edf34862dd584010eae5ab8418108 in C:\nats-server.exe 
# Wed, 11 Dec 2019 18:31:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Dec 2019 18:31:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2019 18:31:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2019 18:32:01 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0591285374eb5389845162a5833b3c4604d58ef1e79438fd4b95fa89f87e13e6`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e0e12dd4f6a98d6b5e98f61b6e0d8ec50d2ed59a985b6c90d93967c930bf65`  
		Last Modified: Wed, 11 Dec 2019 18:35:35 GMT  
		Size: 4.0 MB (3988327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d8866600598ec2c903a8f4d1ff69c723761de339789b2dbe3af27242162598`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ecf0d272921e0a8dda7df2ed6cdbbe00e99ef120e3a4a355ad6780a58944db`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9990aafc65d67a8bc1e7bfe3cbe46af25fd06a367f211c87f1372ad89a7dc`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10b6336a26ba02ed42bd6078c6363be2ce052a4af6cc2464c7fca275ec7940b`  
		Last Modified: Wed, 11 Dec 2019 18:35:33 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
