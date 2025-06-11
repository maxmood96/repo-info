## `openjdk:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:8411d5acab576a136ae40f4da969108c3ecf2282a124a1da853826a61901156e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:ac6df361dcf03aefaf832636ac9ec184866a5e2a26f57e236398718aaea56cb1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410722434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adb21c0e084735690011d77b731f9e391aa3384893c58cf2dc22e513e956c1c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:07 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Jun 2025 22:15:10 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Jun 2025 22:15:16 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:18 GMT
ENV JAVA_VERSION=25-ea+26
# Tue, 10 Jun 2025 22:15:28 GMT
COPY dir:2a5431c9629d8e59dc59f707822e3e4d9048b856e0212fd4224a68120121ffaf in C:\openjdk-25 
# Tue, 10 Jun 2025 22:15:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Jun 2025 22:15:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b5ac83507b673505f004dd89033c360582e5618c4840d7a181f1f6ad22b707`  
		Last Modified: Tue, 10 Jun 2025 22:16:31 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba89929126fd534632face073b9a910ac81219b89624f9ef5f08be22bebabc`  
		Last Modified: Tue, 10 Jun 2025 22:16:32 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c362e746e2340b68691fba051a6567dbcc69b9436ee9481124fa095676c7632`  
		Last Modified: Tue, 10 Jun 2025 22:16:32 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab2cc9a92219992e17eaaf1ad07ac919a3ac727509f56d5897919b803f4bcba`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 75.8 KB (75831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d502afd814c3cd3a4e18b6d603cd08812411f0ebebfb0a0e671382e1537b31c`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e23dbe848b0aaedb55a3768876b07347cb313e5aad67f30c32f3e3ebeb0b5`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d9f88d05b368bb4ad81064b2c55a2d48971bc6656768a86b2eaec2a9e28cb`  
		Last Modified: Wed, 11 Jun 2025 00:23:54 GMT  
		Size: 218.4 MB (218444354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b972f3bd2b070eb7e8697d961a8f369a3fdaf67ce2e076bc8c3e9d892314414`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 113.4 KB (113419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126316482b7d4cbf018959d45cd0a6a78a7eb90bb7627c80cd4dcbf7d1e7def2`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
