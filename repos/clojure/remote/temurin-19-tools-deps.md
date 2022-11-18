## `clojure:temurin-19-tools-deps`

```console
$ docker pull clojure@sha256:d11c31538b360fd466dfc1b85d91972d07c715b0116d137cd0e2aba1db8a9390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:82a5ce09f752b6da598bbb185c7dd88b49bd90b08e3fbb004608320db74262f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302960121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b758209c5379e4172932b09007abae01dd0d54b63662a008c6c28f78edf9cc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:45:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Nov 2022 18:21:09 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 18:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e8d7b3189364afd78d936bad140dbe1e7025d4b96d530ed5536d035c21afb7c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='5f404ae08d7c49f22fe04c04ec39d7e7b17cae2007b9513ad1a7a1164174898b';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_arm_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79320712bbef13825a0aa308621006f32e54f503142737fb21ff085185a61a96';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0b4168e5a98d89b0a24fb2357b3544980d8c88a639024cde18b119b27d7583ae';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='163da7ea140210bae97c6a4590c757858ab4520a78af0e3e33129863d4087552';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Nov 2022 18:21:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 18:21:22 GMT
CMD ["jshell"]
# Fri, 18 Nov 2022 22:28:46 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:28:46 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:29:00 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 18 Nov 2022 22:29:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:29:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:29:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:29:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fa72e018dd1c616d4bdb23d6fbb735820db9a943b470a787973556d4ee24e`  
		Last Modified: Wed, 02 Nov 2022 18:50:22 GMT  
		Size: 17.0 MB (16986189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edabaab1df2cb60a037691c6905e8d3411350c0969896a1e20a84e015767e0`  
		Last Modified: Tue, 08 Nov 2022 18:25:37 GMT  
		Size: 201.1 MB (201113040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a80203ae944000b5b9bdc3a2ca01a7ae404948f58182dd6a4d7ed2c24bd4b5`  
		Last Modified: Tue, 08 Nov 2022 18:25:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c14f1e9c54404819715cd0ccd5e86313c632b20ea837c1c468f7f1b86b790f`  
		Last Modified: Fri, 18 Nov 2022 22:38:31 GMT  
		Size: 54.4 MB (54434090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36514a2446e376b392e89c851fc145442290ae6ab7ffb65404287073756578d0`  
		Last Modified: Fri, 18 Nov 2022 22:38:24 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d889ec6b323eb9bc227024d9dd6e5a7e70b8b0e6d63b64abc7b7c0963b428c5`  
		Last Modified: Fri, 18 Nov 2022 22:38:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3dd36922a819abcc17436967ddf0d4a9d48e34b957009dbfe5dddf80cfb4e193
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301059123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebc884774ee6d4e287a0e595fd4878580bf3ac6ea6aa341339ca7877b492740`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:45:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Nov 2022 18:40:30 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 08 Nov 2022 18:40:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e8d7b3189364afd78d936bad140dbe1e7025d4b96d530ed5536d035c21afb7c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        armhf|arm)          ESUM='5f404ae08d7c49f22fe04c04ec39d7e7b17cae2007b9513ad1a7a1164174898b';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_arm_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79320712bbef13825a0aa308621006f32e54f503142737fb21ff085185a61a96';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0b4168e5a98d89b0a24fb2357b3544980d8c88a639024cde18b119b27d7583ae';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='163da7ea140210bae97c6a4590c757858ab4520a78af0e3e33129863d4087552';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Nov 2022 18:40:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 18:40:41 GMT
CMD ["jshell"]
# Fri, 18 Nov 2022 22:46:46 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:46:46 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:46:58 GMT
RUN apt-get update && apt-get install -y make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove wget
# Fri, 18 Nov 2022 22:46:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:46:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:46:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:46:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8d9c230ad7b20621780183623ce76b7c296e1db90d16a51deeb03f19e2493c`  
		Last Modified: Wed, 02 Nov 2022 19:49:51 GMT  
		Size: 18.4 MB (18416178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05aaebf6b0db47b8f3377a815a4c883dde9e24e0df80eff89a226611b336da9`  
		Last Modified: Tue, 08 Nov 2022 18:43:41 GMT  
		Size: 199.9 MB (199864031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af738d859a999397d35c587ef19723df837a8228e53bd465021e40d77bac1eeb`  
		Last Modified: Tue, 08 Nov 2022 18:43:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c668de206c4ed0199f9397c617773f5fe157d059925715742f7a223343c9d9`  
		Last Modified: Fri, 18 Nov 2022 22:54:37 GMT  
		Size: 54.4 MB (54395567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c007b4da3906394cbf0f010f00bec09a1bd67adb94581e78b1f4cc8c6c0fc4`  
		Last Modified: Fri, 18 Nov 2022 22:54:32 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5238c1be93dc159970c12cfa2069cf0678d26212b9e1e1ec5d306a7bfd2a618d`  
		Last Modified: Fri, 18 Nov 2022 22:54:32 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
