## `openjdk:25-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9ae832fbb9059eb12ee3993bf1644e7db01ceb676488494399c3638568e5ed7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-nanoserver-1809` - windows version 10.0.17763.6893; amd64

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
