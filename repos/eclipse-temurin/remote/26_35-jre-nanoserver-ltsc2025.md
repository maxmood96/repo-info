## `eclipse-temurin:26_35-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:886406a6d1d31a724b26f771aa9807929536cdd540f738e92f0697a4398c3e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `eclipse-temurin:26_35-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:2b7f8c0f2abb7020601eb74ce7313457662abe3bb6e4bbd1ab410b776846984f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.9 MB (259854218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5c3b1e53aa0364d2b0fa348d44d0ec31e1e291269a518b189d13143840d7c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Wed, 08 Apr 2026 18:18:42 GMT
SHELL [cmd /s /c]
# Wed, 08 Apr 2026 18:18:43 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 18:18:45 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 08 Apr 2026 18:18:47 GMT
USER ContainerAdministrator
# Wed, 08 Apr 2026 18:18:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 08 Apr 2026 18:18:57 GMT
USER ContainerUser
# Wed, 08 Apr 2026 18:19:29 GMT
COPY dir:45edd54e05e2fb7ffc611e6ef0c2df37aa13ac9c3c9a476003fc542e9ad17481 in C:\openjdk-26 
# Wed, 08 Apr 2026 18:19:35 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c144822b0666b1af8456aa115f2c1a97a03ebbc50b56210f84b4420be6246`  
		Last Modified: Wed, 08 Apr 2026 18:19:42 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245a2ac6a983e46c44920fa3b45eae3881f4927e18fbf6fcc7a24dd18cebab8b`  
		Last Modified: Wed, 08 Apr 2026 18:19:42 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205c5f08dd92154190c25c1179382df8978e9ebdb736114cf80ac2a77ed94c3c`  
		Last Modified: Wed, 08 Apr 2026 18:19:42 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ab00403b6328ddf71389bd3979948b24e77009b7b0744c0e512d170c17b607`  
		Last Modified: Wed, 08 Apr 2026 18:19:40 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e99edfff3da1a30524b6bcc00dd396e055eef9396270c61bea2fe0cc1f86d0`  
		Last Modified: Wed, 08 Apr 2026 18:19:40 GMT  
		Size: 70.1 KB (70078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226d8ef7ccc7579aeeecb4a823a0ade4e671ec2d68c3bbff761b131eae163e46`  
		Last Modified: Wed, 08 Apr 2026 18:19:40 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d918cd625cc99087790b6a085785aab103f89c056f010caefef9d806e430e`  
		Last Modified: Wed, 08 Apr 2026 18:19:50 GMT  
		Size: 60.3 MB (60266573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034f13ac11841c7a21a05d177839bbd0f8e27cb8398123893274b49e094dae05`  
		Last Modified: Wed, 08 Apr 2026 18:19:40 GMT  
		Size: 102.8 KB (102847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
