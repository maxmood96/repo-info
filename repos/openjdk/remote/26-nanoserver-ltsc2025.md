## `openjdk:26-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:3aacadb0ad834c1fc070ab6cf21ab22537c2e3efc5eb58d3608d3e6792ca725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `openjdk:26-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull openjdk@sha256:88878c146bb64ad3b294e759620bdc8a7ddb2da13ecfb2a405f48edf83d430a2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411831544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f4b20dec51f49c0b2e10c7f5bfb56022caa0df2e2979adee5ba1a103c5d103`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:15:06 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:15:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 09 Jul 2025 19:15:07 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:15:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Jul 2025 19:15:11 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:15:11 GMT
ENV JAVA_VERSION=26-ea+5
# Wed, 09 Jul 2025 19:15:20 GMT
COPY dir:a8af305eda69ca7e4a97e843a96509e487ef158cc8b5f27ab7de11cd1f4c0ba7 in C:\openjdk-26 
# Wed, 09 Jul 2025 19:15:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Jul 2025 19:15:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb0eeba4896ad94f4d28b468e8497defac50a861e152fc9f7c7dbd885a91f2`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1401c7e05950d30fdecc39cf136ae1d07d31877c480e663c7a5c4c2e72925f`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3396cbc3e5e4820ab338d50077a87f97784b18f5d98cd724216458cca6a2e6a0`  
		Last Modified: Wed, 09 Jul 2025 19:16:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fceea0a4449db2fb9acb4e4d39cbdb7234f3679080858b65a765fb941742a190`  
		Last Modified: Wed, 09 Jul 2025 19:16:01 GMT  
		Size: 76.1 KB (76148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cda92b8e310a95b1547dff787ce1f21a22a5b48b966f0db074a486d0af0c8f`  
		Last Modified: Wed, 09 Jul 2025 19:16:03 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032aea473d59d0db0272434bb8ef6be8251bf99046a27efc41fa374553b86425`  
		Last Modified: Wed, 09 Jul 2025 19:16:01 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c0828f68c879a15a3cd274ae9d164b9e9543b33c7e79f95a655d50261950b1`  
		Last Modified: Wed, 09 Jul 2025 21:25:18 GMT  
		Size: 218.5 MB (218483611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2935359a41879ddc2eb76b829dca4f39f938cf0a52854ebc6ddab547391c8498`  
		Last Modified: Wed, 09 Jul 2025 19:16:02 GMT  
		Size: 115.1 KB (115120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e235911944ab9da9fc58fdf0563c52b40f437f8719fad3e13868b7be02f15`  
		Last Modified: Wed, 09 Jul 2025 19:16:01 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
