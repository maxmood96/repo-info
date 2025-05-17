## `openjdk:25-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:d440abd413e075c1ca1b28526b8beea8bbb2dd3f717c4612c887c178d7b16635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:6ace5329eb455c537fb0cb980d51d0d78bb8cea4f11bee1f987a0c6d91733b26
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400529300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804971ff413d602ca8f0e1605e011c2e54a67bcb61329690b09b3828096f2f5e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Fri, 16 May 2025 21:13:37 GMT
SHELL [cmd /s /c]
# Fri, 16 May 2025 21:13:38 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:13:39 GMT
USER ContainerAdministrator
# Fri, 16 May 2025 21:13:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 16 May 2025 21:13:42 GMT
USER ContainerUser
# Fri, 16 May 2025 21:13:43 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:13:51 GMT
COPY dir:be99341787be1c3f0d565e6ac1d9202629ef201376adf519d795dfb5baaa83fe in C:\openjdk-25 
# Fri, 16 May 2025 21:13:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 16 May 2025 21:13:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ee97e4a225f190885c8aa2b7943f296eb6abd10a185ea32a7043b0d4754e90`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b00dcdbb90acf4badb49ebbfa692589ecddab522108848b6ba2b6fe6bd8bbc`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb43016baaf3ae4792eb1133d66a4293c9d74b406d79510bf2e3499a0c710eb`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c13378b2ddc602b53e6227e369089729278ee49599e19f369e360b5417743`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 76.6 KB (76584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2d878af9a1d89335e50590663ea6ff95019d70da97af215b502a2d7e48caf8`  
		Last Modified: Fri, 16 May 2025 21:14:47 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ad6ed16b3f1c1fbda893bcbacd224a0aa46fb28fe2b5dba9483be566ed074f`  
		Last Modified: Fri, 16 May 2025 21:14:48 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a82fb2c7d125ea893de1cbc897b38577a4039d6c265bd744ede8ad5d9ff2224`  
		Last Modified: Sat, 17 May 2025 00:23:56 GMT  
		Size: 208.9 MB (208919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaa4455312e51dfdd23927dac9994417af6b3d63b7ea84d52f6d018e85427ac`  
		Last Modified: Fri, 16 May 2025 21:14:48 GMT  
		Size: 114.5 KB (114494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41933a6ec070fb5ded6fed14447860ea41ed5d54b3fa2ee95dadc7b33fd2cc78`  
		Last Modified: Fri, 16 May 2025 21:14:48 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
