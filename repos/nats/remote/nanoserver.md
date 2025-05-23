## `nats:nanoserver`

```console
$ docker pull nats@sha256:5cc9d495e86b7caa02ed8c6efd98071810a86094d0365b49cd0d6c923575d630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7f1852f9db22e7291125c8af35613f1f24a34c7f83a3172ae053c1374b47d1dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115280860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2beb781651a585bc0a63c840bab3871d9a7401bb08436b206ad674b8b07575`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Thu, 22 May 2025 17:15:06 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 22 May 2025 17:15:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 May 2025 17:15:10 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a73c07fff1a8eadbab3a8c38848875911183270873bbb5e6a0a976ce203047e`  
		Last Modified: Thu, 22 May 2025 17:15:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70695728b4f1e701843b8317a686d44855c7da3371a1cd2d28b29b683fc1073f`  
		Last Modified: Thu, 22 May 2025 17:15:15 GMT  
		Size: 6.5 MB (6494465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4d5d0b8525ea519faeee53b51ff0f617a724effce2c427b032f4526a20982`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0951a16249f9fe6fa46d9356d22c4e163521236dc6bc565dc5a4bfa04710c4b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9249d4c0d1520d254d194e56e1ea972c6d550f97ea9293bbeffbe4f1a77e2d`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e353f5dc214f6f3980cc85fef3a30665c171e0199ab65f24e6b606088e6256b`  
		Last Modified: Thu, 22 May 2025 17:15:14 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
