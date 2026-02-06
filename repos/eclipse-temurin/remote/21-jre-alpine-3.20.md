## `eclipse-temurin:21-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:3ce6d389fc60453114bf9ec58d6082daf052e2410104652c455482846ac794ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7a7b2c801c318162154d1b7e3016889380340c2c196ef36c39ffa02829378093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72880561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdb26ec741b15b303bf4054baae332a3728b0733f8b4235fd332d192002697f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:35 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:35 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:20:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='d1cd7b33dcd81293b0b705f4d0e79adce092786be31736a63abe6a4b31841ae5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='4f6200277644afe6ad49218ae1dd45ab3d0d0b2ac4109163604e36156a93a306';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:20:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304b3fe986811befff6876df0c948866c20c3f41c159bc481eebbf46eba39718`  
		Last Modified: Thu, 05 Feb 2026 22:20:51 GMT  
		Size: 16.1 MB (16081545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e375fe5e660d709e40dece00265760a3234789eaf327a99186dd8100895e04`  
		Last Modified: Thu, 05 Feb 2026 22:20:52 GMT  
		Size: 53.2 MB (53168748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c1bdce5899141b477798861cdf699505695cba0966677247c56f9c87ca634e`  
		Last Modified: Thu, 05 Feb 2026 22:20:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa578596d22c9ccb640a3137041d0c03900ae961e91275c02b33f9eef848de0e`  
		Last Modified: Thu, 05 Feb 2026 22:20:50 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4c88047be02ac6f78dac7f9b5aa3a1295a5a39c5a57fcb3b55e5895082252c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.5 KB (910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8badac8a384795aaa3fa36beb66d0d1d129f6c86206658647a008895ee2bd1`

```dockerfile
```

-	Layers:
	-	`sha256:69d9406ebaa6a0a1be7f70cf652c43ecd1836b17b2416c6a760254baf2f4ab02`  
		Last Modified: Thu, 05 Feb 2026 22:20:50 GMT  
		Size: 891.5 KB (891516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b61b3ed826caecf21eca97e3313596247981c66b895822fec879ca4ea43c0d`  
		Last Modified: Thu, 05 Feb 2026 22:20:50 GMT  
		Size: 19.0 KB (19025 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b89f3041814dfd2562040fce8f8593a750673b2bb101ecc5b4ff28f88c7a5a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72587244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0834c6572af68561728b3e261cdecadbb9bd9640db226d2218c172dbac354e2d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:33 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:36 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='d1cd7b33dcd81293b0b705f4d0e79adce092786be31736a63abe6a4b31841ae5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='4f6200277644afe6ad49218ae1dd45ab3d0d0b2ac4109163604e36156a93a306';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:19:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cdda075426ab79b59f3943e77f261e6dfc3b766de41490827ea1c05498c211`  
		Last Modified: Thu, 05 Feb 2026 22:19:48 GMT  
		Size: 16.3 MB (16254287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52487aba47bb1912444caae24047faa07eb08a13d7d8459bf80bbdde541517d`  
		Last Modified: Thu, 05 Feb 2026 22:19:49 GMT  
		Size: 52.2 MB (52240591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93338a8fd48a737ab202d2657b4e5492db2aa6e2d42070e94e8b805520bf17ff`  
		Last Modified: Thu, 05 Feb 2026 22:19:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fee66470a16f82deef7ff72611e066f3c7196729ea25ae62cf2e1a503b298d`  
		Last Modified: Thu, 05 Feb 2026 22:19:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:68f3110056a64e308df67957866e1ae8e3fa4ff33e38ed9786658b6e3018b3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.1 KB (910065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0879afc9cd072546d9374dbdbb7042adc1961629ab24441ab1eb662333ca7e5f`

```dockerfile
```

-	Layers:
	-	`sha256:ac0d3176fa94b456f2b1526821920b7694afab80dfeafda86f77677480bac79a`  
		Last Modified: Thu, 05 Feb 2026 22:19:47 GMT  
		Size: 890.9 KB (890930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5997e59b434be6963b88f9cc6b94c8b45e5a6c5131024274ff72285574a5c9b9`  
		Last Modified: Thu, 05 Feb 2026 22:19:47 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json
