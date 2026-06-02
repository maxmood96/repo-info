## `jetty:12-jdk25-alpine`

```console
$ docker pull jetty@sha256:52e9efeb3e690e536939c85d8ba2e7df1fdd3fa6577d84345d2ebd52f4e01cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `jetty:12-jdk25-alpine` - linux; amd64

```console
$ docker pull jetty@sha256:545c2026925fb028b582324aeea5f2c58cee7bf80fa6ff2a63761047f75662ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163524538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1b64ccb3d6d80b6622d0cd9ed0ce65485082500601045792a4dc59ee8b56f1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:26:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:26:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:26:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:26:33 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 17:55:00 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 02 Jun 2026 17:55:00 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 Jun 2026 17:55:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 Jun 2026 17:55:00 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 Jun 2026 17:55:00 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 17:55:00 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 02 Jun 2026 17:55:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 Jun 2026 17:55:00 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 02 Jun 2026 17:55:00 GMT
WORKDIR /var/lib/jetty
# Tue, 02 Jun 2026 17:55:00 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 02 Jun 2026 17:55:00 GMT
USER jetty
# Tue, 02 Jun 2026 17:55:00 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 17:55:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 17:55:00 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcd71e97d819f54817ede73936d3ba8e0e56a42c8dec6fffa3dcf0a5f0b4cd7`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 14.3 MB (14307043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069decb9687a1d107c70cc1f3b39e28717aee5b68017f656ac233f17fabf3d80`  
		Last Modified: Thu, 30 Apr 2026 23:26:49 GMT  
		Size: 91.6 MB (91623532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b72908a207a549bc818ba092166eeb02f65c17134d611b1f98600452d5217e`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a11818993d9767c2a1269e3b83ea425a7dbc1d260bf8e8e208ef3eb39c4234`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8c1768ffc2e2df24a797b985f23526e1339e37c0b9495994d55f163ba6d2aa`  
		Last Modified: Tue, 02 Jun 2026 17:55:12 GMT  
		Size: 53.7 MB (53725490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680e277862f238614790574dba9eb6d452ff1ad5025c694249916264b529426b`  
		Last Modified: Tue, 02 Jun 2026 17:55:10 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk25-alpine` - unknown; unknown

```console
$ docker pull jetty@sha256:baabcaabde29d41cdfc3a0e432cb05722e774b1a6883192262111780f449c55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40787eb1afc95c726ad2d7217d88db6e6ab42dd02e89c4feed56c9068f4afec3`

```dockerfile
```

-	Layers:
	-	`sha256:a59503a3cf2ff3f7e5fcbfbbe9094618be77dfe1b3994c606ce657e1e08fc65a`  
		Last Modified: Tue, 02 Jun 2026 17:55:10 GMT  
		Size: 1.4 MB (1380577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6583668215caa5c7ba3fc93ebf392ad523e074e2816088fb54bdc9c78d69840a`  
		Last Modified: Tue, 02 Jun 2026 17:55:10 GMT  
		Size: 20.0 KB (19981 bytes)  
		MIME: application/vnd.in-toto+json
