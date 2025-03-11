## `openjdk:25-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:3ace118a810d685cdaba746562603b22a12c2da6808176286dca8eac476a42b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-jdk-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:dae59f0a703012a0e9708cf0a7848ab52405a12aa7c75731cda0f55279a6adff
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.5 MB (413469265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5604521b977f302b234174163f78b4da2ed11accaed450775e59adc4e030968`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Mon, 10 Mar 2025 22:15:46 GMT
SHELL [cmd /s /c]
# Mon, 10 Mar 2025 22:15:47 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 22:15:48 GMT
USER ContainerAdministrator
# Mon, 10 Mar 2025 22:15:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 10 Mar 2025 22:15:52 GMT
USER ContainerUser
# Mon, 10 Mar 2025 22:15:53 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 22:16:01 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Mon, 10 Mar 2025 22:16:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Mar 2025 22:16:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6384975e3c826b0d7168f7d1234bbc540f11efb184206b1fdfa88ea5bb28bd1`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7473dbe7a78cc9a4b05ae5664fc9a1231ebcde4c043f75836a92883616ac10`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f841f40725853d2cf06f48c366d2b2024f67b9fc8affe7bc22f7c767170161`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be311aa95923e557c660c3e2cfe6d1e2af3d88dafe93898a60d808db3724130`  
		Last Modified: Mon, 10 Mar 2025 22:16:12 GMT  
		Size: 77.3 KB (77343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9269698873f93d2d6c2fcf918b22f538dfc35cdc8c4796ad92553e4e4ba72f`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89b5dd7fa7375fcf704b123db9784dd316b8d30c0dd45667df5144a6d41202`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d82ce82484bff28427e47fd8cab82daa1e4370b9517d6c914ced983fcee084`  
		Last Modified: Mon, 10 Mar 2025 22:16:22 GMT  
		Size: 207.4 MB (207398896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea4510e6131cc06aa41dfa6ed56c3d6a8ae8cf2d56716f32062ef062834722`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 96.4 KB (96413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13617a1a7848553e867202207ab2caf5ebe95f729cd927378fd86d83d58db0af`  
		Last Modified: Mon, 10 Mar 2025 22:16:11 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:17a5bd7b2bb73dfef1373d732100662c1eae33833fa87852ab9cee709ed9b7f2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328261755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07792d9aabf4bd3dd9c4317f1a41236800a362a7b4be86f428ca143f8a71ce65`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Mon, 10 Mar 2025 22:11:34 GMT
SHELL [cmd /s /c]
# Mon, 10 Mar 2025 22:11:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 22:11:36 GMT
USER ContainerAdministrator
# Mon, 10 Mar 2025 22:11:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 10 Mar 2025 22:11:51 GMT
USER ContainerUser
# Mon, 10 Mar 2025 22:11:51 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 22:11:59 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Mon, 10 Mar 2025 22:12:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Mar 2025 22:12:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9da150ea4148ad0207982ead62d436e56e22b37865514aecbdc4b994008e53`  
		Last Modified: Mon, 10 Mar 2025 22:12:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a608914bc4b0f024e9f44bf63980206c8c7537550ae1564f5621cd34470e5a`  
		Last Modified: Mon, 10 Mar 2025 22:12:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96ae180f14b7a3e7cedd9f4f619315428605657860247afade0d649c8bbeeda`  
		Last Modified: Mon, 10 Mar 2025 22:12:10 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b4a178ad55a8bfd2faf5381391bbeb72f4915f2003e9229a3cc07c041d39ed`  
		Last Modified: Mon, 10 Mar 2025 22:12:10 GMT  
		Size: 83.6 KB (83565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c480dc0419ea8d8fd848b8ce031525d2bf4c2d7b72710ec28f61c86d100b799`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87d72abacaf3bf5b966f062a6f3602c063175b55be91e3cea8c0082964f39f8`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5442221df34cb19c389bd2b5d77c78c1a746bb528221125c623879edbf8959`  
		Last Modified: Mon, 10 Mar 2025 22:12:20 GMT  
		Size: 207.4 MB (207399271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebf2d14a6308825e46cb57407e39f4467eddc0db0017e31e4b4aeacabfa802d`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 106.1 KB (106134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2cfdfff175f984e4f9b1dab9dc64910ae88d66a1d4be7813df72be8051c35c`  
		Last Modified: Mon, 10 Mar 2025 22:12:09 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:9666f40b18fce096f31990b3749704b81e3f38b05489fb82d5dfe238bf823aba
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318796133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a70e92791bf16d44351633121fdca426a787940931bf0def81854375f95141d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Mon, 10 Mar 2025 22:11:08 GMT
SHELL [cmd /s /c]
# Mon, 10 Mar 2025 22:11:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 10 Mar 2025 22:11:10 GMT
USER ContainerAdministrator
# Mon, 10 Mar 2025 22:11:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 10 Mar 2025 22:11:15 GMT
USER ContainerUser
# Mon, 10 Mar 2025 22:11:16 GMT
ENV JAVA_VERSION=25-ea+13
# Mon, 10 Mar 2025 22:11:25 GMT
COPY dir:41adcea28f6e8239eac0b74c19049c5daef67ad138ba9db7bdf8df0acc8b0b9b in C:\openjdk-25 
# Mon, 10 Mar 2025 22:11:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 10 Mar 2025 22:11:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63ce650f5c01a002561668b6d128d172240c11436cf909407d068f2bd3c08fd`  
		Last Modified: Mon, 10 Mar 2025 22:11:39 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cc526735de18e53662cd296457220e559e2fd37b43e4601203c806f5782c21`  
		Last Modified: Mon, 10 Mar 2025 22:11:38 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e3c73ff98e9f0ebee87cb418d7268c2b432de15c0c38977848b5166272f893`  
		Last Modified: Mon, 10 Mar 2025 22:11:38 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b9b50038ab98ce6e863c3aecb393fc23b4da3e1feb98d0d726390f07d98769`  
		Last Modified: Mon, 10 Mar 2025 22:11:38 GMT  
		Size: 68.5 KB (68528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11de837225c2eaa4311c470f0d1011f4d7514de7bbb0e88397d73bc0a51555c3`  
		Last Modified: Mon, 10 Mar 2025 22:11:36 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b9fec65de220f8bb520ef72df02db60e50f216b9b166a31a4e1f3a62d01227`  
		Last Modified: Mon, 10 Mar 2025 22:11:36 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454d0feb8e6ebfb879076e638ed09afff5efbf633bdb318c754a07a9f3e3c8cb`  
		Last Modified: Mon, 10 Mar 2025 22:11:47 GMT  
		Size: 207.4 MB (207399573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852d92998ac92efcb876a4675da7254140389ee8b9e4871adcfa8d234f40951f`  
		Last Modified: Mon, 10 Mar 2025 22:11:37 GMT  
		Size: 4.4 MB (4406339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9287d98a5dda45100d1f043d73768c6ea61737c275014e6191a8fdf3809466`  
		Last Modified: Mon, 10 Mar 2025 22:11:36 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
