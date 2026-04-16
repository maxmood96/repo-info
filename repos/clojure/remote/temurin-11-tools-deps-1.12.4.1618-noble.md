## `clojure:temurin-11-tools-deps-1.12.4.1618-noble`

```console
$ docker pull clojure@sha256:498f026dbb888678ca6136954cf54ec265791aec08151a2a702a6adf14c3d319
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; amd64

```console
$ docker pull clojure@sha256:a9f661ab056ae083a9e3f44cf49bea9e3668888b345f67013454dec9f47b16c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247693794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5774e9c1d2dcd8366b7cab524f7dc40dfab7147e820e39fb294ff7548b96cf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:03 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:33:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:10 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:02:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:52 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:03:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259bcdc624a912057aa754687df482d253fa52f4ecde7d816b42bfa092f530be`  
		Last Modified: Wed, 15 Apr 2026 20:33:26 GMT  
		Size: 17.0 MB (16983415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60280751ded65a2e682a2ab378c3fc9a796351e1fab267a226f3ea7878d378a5`  
		Last Modified: Wed, 15 Apr 2026 20:33:29 GMT  
		Size: 145.8 MB (145819268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e015fc8da2e3c44e2c7410290bbf43ffadf1289af0aafa394e83f0c297b46369`  
		Last Modified: Wed, 15 Apr 2026 20:33:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceea77ee92dbbe89b1743c8186e9eafca85b8e102dbe624fe58ff9bef3c9bd3`  
		Last Modified: Wed, 15 Apr 2026 20:33:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1075baa1ba798784720ec9dff236999c45f9f95c8a050fe3bd5252ce53836db7`  
		Last Modified: Wed, 15 Apr 2026 22:03:24 GMT  
		Size: 55.2 MB (55155047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dee46bebb200a56749fce4117c878718f76fca60ae872ea9d89c69fd17adabb`  
		Last Modified: Wed, 15 Apr 2026 22:03:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:f55ee7e3707711fdf0d710cb2d7654152dc8d3cac0048e181aea4bef04a6e15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fced18288ee01d5f95d156fffffc53d83f2aac5a61cca3f0ae7cbf1fbbd7d0`

```dockerfile
```

-	Layers:
	-	`sha256:52271d4f04921bc145ce733e4966b6acce5e356832631e7dd0d147dd24b5c22b`  
		Last Modified: Wed, 15 Apr 2026 22:03:23 GMT  
		Size: 5.8 MB (5775513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101d0f564a64346168b0243b2322e1ccb5a0f5a22b4d326046664545fd7bf43f`  
		Last Modified: Wed, 15 Apr 2026 22:03:22 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aef4bff9eeeb46cfae8a560fe33e5815ea63eca75c9bcd72290d011127aaf6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243490152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7accdc51faa09b3287558f49b621d98ed2685de92b63a373434a2ae9d7882f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:24 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:33:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:31 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:14:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:14:18 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Wed, 15 Apr 2026 22:14:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:14:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57e12f19a04b5ac9e1a6bd3ff16544bf8e32e25bbe05c07e9af1de9064224ea`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 17.0 MB (16996196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d051c925caddc27e15fb896e85e25957e80cb155fa0f58152964eef48a1dd`  
		Last Modified: Wed, 15 Apr 2026 20:33:51 GMT  
		Size: 142.5 MB (142513589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f15fe7227a0a815386947fb45f060258e49a2f1a7676f01f4949b72be68768`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776b8c511c610219bb1baa901cb7773f0737c0d8ea7cff702d9aebb36e146807`  
		Last Modified: Wed, 15 Apr 2026 20:33:48 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598632ab7ebf199ab229875c4da47f4af620f26667361b3b51253a807a11fd44`  
		Last Modified: Wed, 15 Apr 2026 22:14:53 GMT  
		Size: 55.1 MB (55101500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa04cb06ac86451215c543e8d81700f57367d38df71f9d192bba0cd197b5b93`  
		Last Modified: Wed, 15 Apr 2026 22:14:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:28a5c5171f7908a7ba158439f97e0712b6482b9861dc6ee6e93a263721ef7580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3ce6cb06059e1daacf748c18c3d28a6b0be75d536e722a853d4112d5bf7aca`

```dockerfile
```

-	Layers:
	-	`sha256:a1a18848c0f74c56414ee7fda322628c3afd9006a59ec5223cc143ffc69d4ae6`  
		Last Modified: Wed, 15 Apr 2026 22:14:51 GMT  
		Size: 5.8 MB (5782719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7412f1121c5bb876f40c8d12e9eb71a4121fd09bb4115df7d8ec65da9bbf6fe3`  
		Last Modified: Wed, 15 Apr 2026 22:14:51 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:4bc2a091c15b39096ef5004c6c431ee39ff74dfecf3f543015fd9d5358f5f104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245917081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157626bbdb726aa6627f709787888e0f653a6164ab1f757fda677a0cf17dc70`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 04:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:26:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:26:01 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:26:01 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 04:27:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 04:27:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 04:27:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:27:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:27:53 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 14:30:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:30:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:35:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 14:35:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:35:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d800c8df15b3edabc2d41fd12584d685162ec3e3407bdd29445e3916467625`  
		Last Modified: Tue, 07 Apr 2026 04:26:41 GMT  
		Size: 18.8 MB (18813117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a220c00f58cce4caec204896167dc168c2256b2b53fa887a51fa66eeccbc5b1f`  
		Last Modified: Tue, 07 Apr 2026 04:28:26 GMT  
		Size: 133.0 MB (133004967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c58ce451ad0981433298447fb3f692b8c3483469ea9d36516505fd460a9a8`  
		Last Modified: Tue, 07 Apr 2026 04:28:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f113810f8354a10896c0eaf92f06a48327ff4c0bf1e24f3557cb1984b01bdba9`  
		Last Modified: Tue, 07 Apr 2026 04:28:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c2a6d53bdf21d55e194d0608a09a82ad59d28c9f838535efaceab9068c2786`  
		Last Modified: Tue, 07 Apr 2026 14:35:45 GMT  
		Size: 59.8 MB (59782574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3007d2b71eab6e0ad15d25110eb1d0de958a82490693c8d2d5d57a0a82e4a9e`  
		Last Modified: Tue, 07 Apr 2026 14:35:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:89c0eb2db7239f376370b76933b682ce0f16dc904edccd8850f8abea62f4d983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e820a99fa9992392257d1b4d9fb384f48fffa2df46394e1ead2d9ff9f32038`

```dockerfile
```

-	Layers:
	-	`sha256:ee5b55231c7b9f167b88fd37ff3a743df3745c6e001b271f74b5cb1e9ea5d8e1`  
		Last Modified: Tue, 07 Apr 2026 14:35:43 GMT  
		Size: 5.8 MB (5780143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfec70ac237b66f8634071870656faaf5f89c5af7c49924466fef1ddf3d3aefe`  
		Last Modified: Tue, 07 Apr 2026 14:35:43 GMT  
		Size: 14.2 KB (14240 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - linux; s390x

```console
$ docker pull clojure@sha256:0c3952573981bc74115bf7c2761826c912397e552c6f0f04401111dd01d6a503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230578399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1650712fbbfa9fa8520aabcee001ce7665027cb2d56d87c0661b2861e6accc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:09:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:09:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:09:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:09:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:23 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 07 Apr 2026 03:09:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        arm64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        armhf)          ESUM='1ef020c2215f3169c7610df573581806c58f00a0a1d512fd945a2687cbed1173';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64el)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:28 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:39:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:39:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:41:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Tue, 07 Apr 2026 05:41:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:41:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafd1916c5cba31aaa22e1e52aa83c9c76d6979e0d05bbd0bccbd399520dd951`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 17.6 MB (17579082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b6b54faf1d0b905618d6c72981d0b30b7342ea2dde4805dc122eff6b8174b`  
		Last Modified: Tue, 07 Apr 2026 03:09:54 GMT  
		Size: 126.6 MB (126566100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b4944bffc81c057fa6031b471300cb088996165b8c0ae0219dde861cab1abb`  
		Last Modified: Tue, 07 Apr 2026 03:09:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69899eb0c6daeaca16e7d61f72a2166b79ad0def7c9347df5ee9c033b2b7d5`  
		Last Modified: Tue, 07 Apr 2026 03:09:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80e7d1f6f67e5f8d9d7ecf08f3fc408d4b480b7743ff089333587b4d4775fa6`  
		Last Modified: Tue, 07 Apr 2026 05:41:32 GMT  
		Size: 56.5 MB (56518289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f9c37b18ea8d2a624103ccb481bc92d7d0bd6d556333ce54b4be9d9227c1e`  
		Last Modified: Tue, 07 Apr 2026 05:41:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d37d1ef57fce1edd7d817122c13f478e00a9654e61e1b1544ebf0617c40bc2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5787044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000b7fa152ede1501a611a794067eac32c72139bf45e1cc6755ac93d6cb9985b`

```dockerfile
```

-	Layers:
	-	`sha256:073f21a4ec4d3c3bc1f39e0d8d9ceb180d8955f29df5a59514cecac9fd606d67`  
		Last Modified: Tue, 07 Apr 2026 05:41:31 GMT  
		Size: 5.8 MB (5772853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9341518daaab3829f5597eb8f4345d0776a2ca206d0f1088c5dc3bff3e6ba618`  
		Last Modified: Tue, 07 Apr 2026 05:41:30 GMT  
		Size: 14.2 KB (14191 bytes)  
		MIME: application/vnd.in-toto+json
