## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:507c5f84fdd8d67ae09e1a8b0b2d0658d480966bbdf24346008302cb5885e54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:eeb359a0ca361f7a2ff730023bca6bcdddd0ca0d1412e87554a9360f1fad5c9d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105027949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262a266c1062a81eb67f96245b8b6dea8e7b0008705ce7051e8783785ff68076`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 04 Sep 2020 19:46:30 GMT
RUN cmd /S /C #(nop) COPY file:0b6475b59bf6bfe6c1030fd41ea501af74fd46ae70fd98c58683b35f8ed498ff in C:\nats-server.exe 
# Fri, 04 Sep 2020 19:46:31 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 04 Sep 2020 19:46:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 04 Sep 2020 19:46:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 04 Sep 2020 19:46:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d4dc8c52ad1ff0fc383e64c11688e98d786a5f5409e1367d05cdb80b2db887`  
		Last Modified: Fri, 04 Sep 2020 19:50:48 GMT  
		Size: 4.0 MB (4037963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6dd2505c3f76661a7f8f43bd3c5bbace4158d66914091710d55ac929b69b44`  
		Last Modified: Fri, 04 Sep 2020 19:50:47 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eb47d1ef65e0d4d95aca8e6874ce099026a2626edfe488ef880b5bc19f4102`  
		Last Modified: Fri, 04 Sep 2020 19:50:47 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecc4c9a56ef41700f167e7f35a916684fc48167e7bd100072d6760e0ae166a9`  
		Last Modified: Fri, 04 Sep 2020 19:50:46 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eaf2a3d43bcc4b2832d9401813b736136a6e81ad7bca4cdcd59d66bdfeb5ff1`  
		Last Modified: Fri, 04 Sep 2020 19:50:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
