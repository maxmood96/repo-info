## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:f46ab2b445447958bb2f6f3da57dfd6dc2ef67ce56a2809a28360cc82eb4230b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:60f841409f81055954ccfc7c00ab2c8091a55ad7e74167749d6cce9210eb08f4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328245693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d881cfb17878dd9c8af4e28d334eccfa9aa6384ea7f916e3af22b53466fbff3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 29 Jan 2025 00:27:39 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 00:27:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 00:27:40 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 00:27:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 00:27:58 GMT
USER ContainerUser
# Wed, 29 Jan 2025 00:27:59 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 00:28:07 GMT
COPY dir:8eaf4d943fad5808ffdf3732eba720fc3864b955a0e8f89e481534183a904eb4 in C:\openjdk-25 
# Wed, 29 Jan 2025 00:28:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 00:28:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0cbd2f5c45b30ab534c67fa51d78fbdb1f9b2224fc39e14b1a3b179fc6fe1`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2e88535d8fc3649cda90510f7d175dfa1ef7afec987e4d5c1aec913c2c74af`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e16bf76154bdf25696cd33f6d25edb75d192e226e6b1a3ab426284364bb10e`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9077432da026e834e5031e44b312b5962552b66eb0be4878cb3403f7bf35bab`  
		Last Modified: Wed, 29 Jan 2025 00:28:16 GMT  
		Size: 88.2 KB (88153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5715ed4e44985ad222ed284344204f573a3fd08d81ecc93d7e043db8a4737bc9`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47560958a79222fe077868af453176cfb888c2e0152c9cf224cc461ec26ad6e`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d06e42d5bf81b13ec6c5051949bd862d0d91a1acf941790d7f86713e3966c`  
		Last Modified: Wed, 29 Jan 2025 00:28:26 GMT  
		Size: 207.4 MB (207391839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097fd667c97dac8579cce6c5c20a8ba44721246d2d36e48127ad15c81b71285f`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 97.8 KB (97752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d151f1a0d1732ea10050eccc668504f0405517a30cee02b2022a9d1025277e`  
		Last Modified: Wed, 29 Jan 2025 00:28:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
