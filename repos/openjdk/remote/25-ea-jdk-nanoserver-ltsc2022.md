## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:fd7b1f55a53197b84aa792de21ec738201ca598925f1f5ba84a2b978bc63817b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:da132e7e6a992de5394b9289d996554460f20b00d4b1c92b5343249e0ede30c5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340882453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af630e9d73bda650a39a4c73d9483f926a40e46faf8c569d98aef5f84c111fae`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Fri, 30 May 2025 17:57:14 GMT
SHELL [cmd /s /c]
# Fri, 30 May 2025 17:57:14 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 30 May 2025 17:57:15 GMT
USER ContainerAdministrator
# Fri, 30 May 2025 17:57:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 30 May 2025 17:57:38 GMT
USER ContainerUser
# Fri, 30 May 2025 17:57:39 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 17:57:53 GMT
COPY dir:bd2747e79afdad77e7098a4e268355ea8695f52ce1251320a131b555b1a0c1b4 in C:\openjdk-25 
# Fri, 30 May 2025 17:58:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 30 May 2025 17:58:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f73c9e13488ffaecf6beac0f6ffef38fe8a66aec468e3d56ddaa9ecc4aa5317`  
		Last Modified: Fri, 30 May 2025 17:58:08 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b41023021f0ea4683e8625a93d7c09fc56e3159545407a8dbf938a7bda78c2`  
		Last Modified: Fri, 30 May 2025 17:58:08 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc729fc215cfd34b2a1615f34a0b5eaea15581fb175e69cc40e9aa04fd5fb8`  
		Last Modified: Fri, 30 May 2025 17:58:08 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ae011d72bb1ee3f04481b8d987a4f78de856c6d9a0fd410193b30e07ecbff5`  
		Last Modified: Fri, 30 May 2025 17:58:08 GMT  
		Size: 84.0 KB (83980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bea2f3db731464666dc3b8be70249f1550f246c0453674d6a6a9d00733979a`  
		Last Modified: Fri, 30 May 2025 17:58:06 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce526c7c38ecd5ff0e858524f16bb6fa831c7ab677e1bdc80f3b259115d079e6`  
		Last Modified: Fri, 30 May 2025 17:58:06 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bde222bc6114f1abcb0cdab2a80aa1cd245a99533ad0ed67f7b6d020a81f842`  
		Last Modified: Fri, 30 May 2025 17:58:18 GMT  
		Size: 218.1 MB (218116911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d7baf24889ab2c29cc10fb6eae0ab312c5ad5f6c990ad29eb5385e1e393a46`  
		Last Modified: Fri, 30 May 2025 17:58:06 GMT  
		Size: 98.5 KB (98482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878c6f1dacb5e91ded5a673f2a9ff7dd3e7227498df68dd53650cc8cf79fb2a0`  
		Last Modified: Fri, 30 May 2025 17:58:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
