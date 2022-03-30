## `eclipse-temurin:18-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f3e6641319fae848f097e1070159c4eb4c88ebeb459a8a502396ecbc1a052251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `eclipse-temurin:18-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull eclipse-temurin@sha256:a23ebe60c4bd26709345862fb889ce3e9ecd78fad384f4d25a4bd96ba420e5d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293009684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a52d80860b3044235e175314dca7952dd16759e50e71e3d2f5de06cfb784fc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Tue, 29 Mar 2022 19:21:07 GMT
ENV JAVA_VERSION=jdk-18+36
# Tue, 29 Mar 2022 19:21:07 GMT
ENV JAVA_HOME=C:\openjdk-18
# Tue, 29 Mar 2022 19:21:08 GMT
USER ContainerAdministrator
# Tue, 29 Mar 2022 19:21:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 29 Mar 2022 19:21:20 GMT
USER ContainerUser
# Tue, 29 Mar 2022 19:21:33 GMT
COPY dir:2e742036aad301ef262998624b1ad05a0be865b4697e1fe99b4c522724f72462 in C:\openjdk-18 
# Tue, 29 Mar 2022 19:21:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 29 Mar 2022 19:21:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b4ea2f6ec3e6055e456f34267907035db9a099f99f450abd59b36577e0053f`  
		Last Modified: Tue, 29 Mar 2022 19:27:03 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d24521e247c08a0c006572c517748102c74de2d8e724aea0c16ae75d3c91fd`  
		Last Modified: Tue, 29 Mar 2022 19:27:03 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473e74001513b1881b9f197a989bf80b258165bf8475bd6b02b44ba09f91f877`  
		Last Modified: Tue, 29 Mar 2022 19:27:02 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6ae62b1d8a0f4ce864bb1ebfd70c33448571196b915d02f58694beb4234717`  
		Last Modified: Tue, 29 Mar 2022 19:27:00 GMT  
		Size: 72.4 KB (72366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577cef18b63dff61237b1f8f17d9760d2cc42ec8181eecf6e363d74c5020d9d9`  
		Last Modified: Tue, 29 Mar 2022 19:27:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b6fb3f72e6912dc1ed8adc63ca9ecd6808ee059ad65e9323c56e0a95cc314a`  
		Last Modified: Tue, 29 Mar 2022 19:27:18 GMT  
		Size: 186.4 MB (186352754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28c4026d105c90980955c29f766ff517d32e1136ed6e18b5ea4589da124f0f9`  
		Last Modified: Tue, 29 Mar 2022 19:27:01 GMT  
		Size: 3.5 MB (3523676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1cccc47c6df9c078c22786d60d6676ceac33e2a094bd60aafd34352da5a14e`  
		Last Modified: Tue, 29 Mar 2022 19:27:00 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
