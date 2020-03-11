## `nats:nanoserver`

```console
$ docker pull nats@sha256:dfc98e20dd8937bc3999ff0aeb9dba6ad083f67cbad65fab02736d1bac4fa135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `nats:nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull nats@sha256:0e2a7ac695de304cb1fecfba664373220323251f9dbb5774f1bd9d30b80f99a0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105076708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4979f079d35a78c7e29279edbfa6f79d884a4389572a6d2f34a6fe0d5f83c3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:47:10 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Mar 2020 14:47:13 GMT
RUN cmd /S /C #(nop) COPY file:f99d86aa471be86e0fcf1696428f084819e5f50c8beb0a51a30eb19162592f16 in C:\nats-server.exe 
# Wed, 11 Mar 2020 14:47:15 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Mar 2020 14:47:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Mar 2020 14:47:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Mar 2020 14:47:19 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:11472ae705112ae5e29e58c937ca3e026bd8eb756b2fcbe538bba856f7d80ff9`  
		Last Modified: Wed, 11 Mar 2020 14:48:32 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de639ff378eb1cba62ed72669f24c0a2361a2455247dc20431fb6507408517d`  
		Last Modified: Wed, 11 Mar 2020 14:48:30 GMT  
		Size: 4.0 MB (4021116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c8c22764ac29b9180c8b91e0d8a3b7e33a3a74bd9334cc6e1b6300981c19de`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018dc0a8631a1da4c6a6347bcdd9d446de450f2e276dda808fba9e2d03875f12`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36a2656265ef8378c9ec6b2df8add1f4f738208b90c964e5812c07f83031f5`  
		Last Modified: Wed, 11 Mar 2020 14:48:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ec88c0f8aa382d4f8979f8fc0d6df4371ca0a1b05593ba8fa27e9a51a2e477`  
		Last Modified: Wed, 11 Mar 2020 14:48:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
