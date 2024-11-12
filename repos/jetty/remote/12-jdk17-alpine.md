## `jetty:12-jdk17-alpine`

```console
$ docker pull jetty@sha256:5342a79059ff615e0eb1ce9488ca3444924a1fda93c5e1dd6c88e1a30d3e9756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:12-jdk17-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:f9d13baeda26a740eaa39420b81fbfd3eab2fd2ef0298627b6dded87cdf93c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205527904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35dfeaf0858595f9b3a9cb9f1f44571a9cda9cb2ed9242cc9fdffbeb79a66b40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='67632ee4563e9827b56f62ab6da95bce200d9e82092b211988c0d2113abc4071';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["jshell"]
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_VERSION=12.0.14
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.0.14/jetty-home-12.0.14.tar.gz
# Wed, 02 Oct 2024 21:05:31 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 02 Oct 2024 21:05:31 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
WORKDIR /var/lib/jetty
# Wed, 02 Oct 2024 21:05:31 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 02 Oct 2024 21:05:31 GMT
USER jetty
# Wed, 02 Oct 2024 21:05:31 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 02 Oct 2024 21:05:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 21:05:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c672380d9e6c1adbb4a6d4022eb294e5b840ad2dfdb200f7666d2347d8785`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 23.0 MB (22953395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f906cb517e9f117723f09bd4f24c42b6e0db41d2465a2b09bba69e65ffb95e`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 143.7 MB (143689002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2bd53639fc30cf5eddf18027f47695541b28435d6281a1a15c32da7ca9aa58`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9f181b9a20026da33fd930467819ec964e7d1cc60357c69cf9893e2ef55103`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f792a70b979bfc9e01b2e34025d50ff068fc984d05d3bcaa9cb2715dda33abe`  
		Last Modified: Tue, 12 Nov 2024 03:15:24 GMT  
		Size: 35.3 MB (35257528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ab3a3f4184d8f3c835528ad049144aee9da9029f88a19f34ab73ccb8fff78e`  
		Last Modified: Tue, 12 Nov 2024 03:15:21 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk17-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:38c219b194e1d91aaa04793264c96d38d8e724287178251b3e53b7c15e81c8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550ad71e6849656d872776c745e2845a832db5d8fd3af967979ba2baa5bcb7b9`

```dockerfile
```

-	Layers:
	-	`sha256:b6e784682a8b2b13c598a400b162e378ce2cb652bd1add2e53e109595eae11df`  
		Last Modified: Tue, 12 Nov 2024 03:15:23 GMT  
		Size: 1.3 MB (1308164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab61890a8d88677fac3877aa9a4cbc49d8344c29b2abacd76427edf7679f8f2`  
		Last Modified: Tue, 12 Nov 2024 03:15:23 GMT  
		Size: 20.0 KB (20030 bytes)  
		MIME: application/vnd.in-toto+json
