## `openjdk:27-ea-nanoserver`

```console
$ docker pull openjdk@sha256:0174af2199a5d42ab800797fd700d6bf04ab869e7df415d27958bf236c4e4abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:ad8e84a48b2634991ea55d6dce8e90be359a1a9c489f8535e2e2678205d70658
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.4 MB (423436228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23eb013cde42a7a1e62452d2b124503f58c785c3b729637b593aefa92dfa9f0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Mon, 26 Jan 2026 23:14:41 GMT
SHELL [cmd /s /c]
# Mon, 26 Jan 2026 23:14:42 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 23:14:43 GMT
USER ContainerAdministrator
# Mon, 26 Jan 2026 23:14:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 26 Jan 2026 23:14:50 GMT
USER ContainerUser
# Mon, 26 Jan 2026 23:14:51 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 23:15:36 GMT
COPY dir:70f85d11e72fbae24cc84d660c242da927e72cca58a6ae86631f6d18b6f9801a in C:\openjdk-27 
# Mon, 26 Jan 2026 23:15:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 26 Jan 2026 23:15:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6504373a3bad394c538c7bb3fff9d99258473759fc552fb769d6e62e33ff66f`  
		Last Modified: Mon, 26 Jan 2026 23:15:53 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7b0990e2001fbc097db9fcf75d9c98822ad16c722e04499b20e791a120822a`  
		Last Modified: Mon, 26 Jan 2026 23:15:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c1f040c0506ee158c0e626b7a53046a9c6a1d7d80787190d76b0ed4470a0c2`  
		Last Modified: Mon, 26 Jan 2026 23:15:53 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0491e4112c20d97707bf8b3f0d55377ef2123f7ff567ba87a60358385d97219`  
		Last Modified: Mon, 26 Jan 2026 23:15:53 GMT  
		Size: 70.7 KB (70671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ad0a0f21859fb581f5783f3d9f5990134297e93faa38646496ccdd89182fd4`  
		Last Modified: Mon, 26 Jan 2026 23:15:51 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9007088ce331617fa6a240b668df505bbce8c04f4a491b517a05260373b05b6`  
		Last Modified: Mon, 26 Jan 2026 23:15:51 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce96ffed489f0dc2842aa88e384129547f7425564f458b25426bb32111c1c98f`  
		Last Modified: Mon, 26 Jan 2026 23:16:07 GMT  
		Size: 224.2 MB (224199442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd949d26caa0af162ba223d86f104c9e41546c1462b458500c64d6b855b1999`  
		Last Modified: Mon, 26 Jan 2026 23:15:51 GMT  
		Size: 83.1 KB (83146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ac33d9a9ac19531b0f121599da8df24067754e986bf51b378b05a62102a616`  
		Last Modified: Mon, 26 Jan 2026 23:15:51 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:afb34e253c491cb97db8187407794f74e5fa43904909aa5ebe1e26daf6689e2b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351137317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17962292fbf752abd1c7bc4ee8fae944eb08c00a3db12c213bfc7fc9686ef1dc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Mon, 26 Jan 2026 23:12:36 GMT
SHELL [cmd /s /c]
# Mon, 26 Jan 2026 23:15:03 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 26 Jan 2026 23:15:04 GMT
USER ContainerAdministrator
# Mon, 26 Jan 2026 23:15:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 26 Jan 2026 23:15:07 GMT
USER ContainerUser
# Mon, 26 Jan 2026 23:15:08 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 23:16:15 GMT
COPY dir:70f85d11e72fbae24cc84d660c242da927e72cca58a6ae86631f6d18b6f9801a in C:\openjdk-27 
# Mon, 26 Jan 2026 23:16:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 26 Jan 2026 23:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e51f20a630010d929dc6108e426f6d138555f634eb15711b6e888053888c8f`  
		Last Modified: Mon, 26 Jan 2026 23:14:23 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f814946152b30164b4b7b95da9bc5f4508a25062e41ac0959d4285ff71d7a95`  
		Last Modified: Mon, 26 Jan 2026 23:16:35 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4854d0385a1c94cd9703cd42bbe5f337ea64d05f4d0b7b3b4a93753596683c7`  
		Last Modified: Mon, 26 Jan 2026 23:16:35 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d8fb1b64665e37ec66e98637cc0b062e7351d42fd84dd4d7137da03a01b503`  
		Last Modified: Mon, 26 Jan 2026 23:16:35 GMT  
		Size: 87.5 KB (87490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888dd32642ea1c391e89593ddf7d0e978e7d2ceed5b1cd8006b8ceda750db4b5`  
		Last Modified: Mon, 26 Jan 2026 23:16:33 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a6caa58dc854278600d1e7866dd2ab3cb1044a6c37864f6346c8dbddde263`  
		Last Modified: Mon, 26 Jan 2026 23:16:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e81113f50efb92a48afc3c13d9aba08de0b87696baeaace510ace357dcdaab`  
		Last Modified: Mon, 26 Jan 2026 23:16:49 GMT  
		Size: 224.2 MB (224199533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd39330ba671926aee67f9c00527dc9c3568bed114fe9647416bf3ddcabdf610`  
		Last Modified: Mon, 26 Jan 2026 23:16:34 GMT  
		Size: 147.1 KB (147068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2f59f80c166cf17b986cd12c882eb7741f3498878bdbdaf9933636de7c8f0`  
		Last Modified: Mon, 26 Jan 2026 23:16:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
