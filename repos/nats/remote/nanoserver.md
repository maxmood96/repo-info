## `nats:nanoserver`

```console
$ docker pull nats@sha256:1f696d61a391f18ef766caad529a50b4cb5ae17ccf034f2a284cc613ffe4bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `nats:nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull nats@sha256:c6f5c0290b69af0858074f5d517a0c860ba98ed630844922a79fea8878aad5b4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129040730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be630e0c7a9a58ecc3d8536217e7ac74b97cc59a376917899e4feb15c2ba8f68`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:19:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 10 Jun 2025 22:19:57 GMT
RUN cmd /S /C #(nop) COPY file:c0858fd1cf951ef85fbf4130ffdd4b4bf3159ce5e3f5e49a5511a093a63cc153 in C:\nats-server.exe 
# Tue, 10 Jun 2025 22:19:58 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 10 Jun 2025 22:19:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 10 Jun 2025 22:19:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 10 Jun 2025 22:20:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ceb4d6f532869b91e81807ba56db9c4fae6c56b93ea65b408299edaaf5e6bd`  
		Last Modified: Tue, 10 Jun 2025 22:20:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d042c1da6da9e22814ecd7a30d14a484237aa0aa844385a97b65c8d11e309b7`  
		Last Modified: Tue, 10 Jun 2025 22:20:35 GMT  
		Size: 6.5 MB (6494405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8f51c48fab42ee0087b7b6e2efc13dcedf15a4f13e16c5a3783f49711565b`  
		Last Modified: Tue, 10 Jun 2025 22:20:34 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a95f84b7e259ca3ad002fd34a995e4309c8e760efe812e02f4f77364c8bf025`  
		Last Modified: Tue, 10 Jun 2025 22:20:34 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb7d6f1838f4c3bf77c670b025305d0e11adf15167e7f3c422992352b54cbc4`  
		Last Modified: Tue, 10 Jun 2025 22:20:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b745a844a9ebf8409403f624605c39bce78419fa31c89fb7010e04347ee29`  
		Last Modified: Tue, 10 Jun 2025 22:20:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
