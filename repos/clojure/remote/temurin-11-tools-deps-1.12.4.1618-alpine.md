## `clojure:temurin-11-tools-deps-1.12.4.1618-alpine`

```console
$ docker pull clojure@sha256:f59e3c308ef3ef441562acacc53f0ed43208bfaddf337272179bc686739fe583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:c0d92970b1a2650282724a1fcd7fc56d6f51886342535530477d4d8631c3c548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187060250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5920010d317fbb4c34f9edce0abc482ac68e9c2cd5edd3640d0db2e5c1a167e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:32:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:32:56 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:02:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:31 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:35 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 15 Apr 2026 22:02:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:02:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec914d871e26d0465399fedbb12a944add78359e4bacb45111654e407011389`  
		Last Modified: Wed, 15 Apr 2026 20:33:10 GMT  
		Size: 16.8 MB (16837789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e0f2de0712b22eb820b820ec9d10381f0162a40034dd9db90063cf9bc5b7f9`  
		Last Modified: Wed, 15 Apr 2026 20:33:13 GMT  
		Size: 140.9 MB (140916718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97836bb5bbf19dc634eaea3ff5cfbc9b0ca22932b1bbb49c9a806a0bb040b842`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c470514f36b76e7d4fbd25626009aade331446b35fde7acb2f42ae8b0b5c53a1`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1238780b79e7ae3829f865bad47de29e9e890106a0f160862ade457f439ee2`  
		Last Modified: Wed, 15 Apr 2026 22:02:45 GMT  
		Size: 25.4 MB (25438500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12491f42406ed1667a8c25af751b7972d91f9bf86fee2de30514eb8fff6509cb`  
		Last Modified: Wed, 15 Apr 2026 22:02:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:8191dd82b9723e958e5782f99ae356f130527d191e2b8a58999328ff576da2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1225798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f2b81d8ad5e35327a7986e264ad28bbede247d8af5dc079a81f456b5bdf611`

```dockerfile
```

-	Layers:
	-	`sha256:aaea029e20e3b20ea811e6019ac18ca37df7e5a9ccf1f664daaa4c220cb154e5`  
		Last Modified: Wed, 15 Apr 2026 22:02:45 GMT  
		Size: 1.2 MB (1212404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe3699cf2fdb4f45417de369744b7064ed2bab4d59299744846be79a52a6ead`  
		Last Modified: Wed, 15 Apr 2026 22:02:44 GMT  
		Size: 13.4 KB (13394 bytes)  
		MIME: application/vnd.in-toto+json
