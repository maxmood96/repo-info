## `jetty:9-jre21-alpine`

```console
$ docker pull jetty@sha256:07b2ef9cb0a144d98e4c956f8f7efd0fb40ff43d678b94186d2d56458bf34aad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:9-jre21-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:46a03c1e73ddc085677c619dc7e82def90303385e4a40c54e8f24d1a5f4af1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84158307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d1f84cdaf5dde154bce687394f9a195192f8f6be8a5f9b3ade136750d3f61c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='bcd459e70cdddaa6ada0d855ce944c592814042f1e12d53aa08fa89eedcdf893';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='2330f38feb59ab7af0e2fffc12d5500005d35f7f53f49dd8a9f9aa1ae68aee5f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_VERSION=9.4.57.v20241219
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.57.v20241219/jetty-home-9.4.57.v20241219.tar.gz
# Tue, 14 Jan 2025 05:07:03 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 14 Jan 2025 05:07:03 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
WORKDIR /var/lib/jetty
# Tue, 14 Jan 2025 05:07:03 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 14 Jan 2025 05:07:03 GMT
USER jetty
# Tue, 14 Jan 2025 05:07:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Jan 2025 05:07:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 05:07:03 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ff0155cbec0e1194e65c05ccd8ce6b771b34f8e854a429c48ba2dfa8a1d12`  
		Last Modified: Fri, 31 Jan 2025 01:30:47 GMT  
		Size: 16.1 MB (16135256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a997c76584ddc6c88a725b8c369ead1e1f80d8355f4a28ca9cc2174273603`  
		Last Modified: Fri, 31 Jan 2025 01:30:48 GMT  
		Size: 53.0 MB (53042557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198aafda557c25e9bd92b0730b851eef6dbc7d66526e35901d44fc77a5449be4`  
		Last Modified: Fri, 31 Jan 2025 01:30:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a9ee36b9831c6ff728463b4e54762948f7c6cf33e8516b4fae4ea86a119eb`  
		Last Modified: Fri, 31 Jan 2025 01:30:47 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7388e914e8d24fa4f73694de151b0ff6043eecc0c7c4c56c493761f76d8b9b`  
		Last Modified: Fri, 31 Jan 2025 02:14:28 GMT  
		Size: 11.3 MB (11334681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6353d91ae27b6de2e0c92128f210ceec6a0affe53035269899f631601a90bfed`  
		Last Modified: Fri, 31 Jan 2025 02:14:27 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jre21-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:72413b28d0b9f5aaf3b52844764d5b48bdc95f17612389ea7e3f6815199436bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1017847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bf24de9e9a686c2f05c71d11e14d6ad35a86d622aad07ba34a8442ce18f3ee`

```dockerfile
```

-	Layers:
	-	`sha256:efc671be05451b242c0d36566970216d73dfb7016a46838917f5b8dff7261322`  
		Last Modified: Fri, 31 Jan 2025 02:14:27 GMT  
		Size: 997.8 KB (997799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee9aee15ee12441f406d08b58bb1b8fd31bc5d4e5c1d475a2d009ccdc176fc3`  
		Last Modified: Fri, 31 Jan 2025 02:14:27 GMT  
		Size: 20.0 KB (20048 bytes)  
		MIME: application/vnd.in-toto+json
