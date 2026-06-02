## `jetty:12-jdk21-eclipse-temurin`

```console
$ docker pull jetty@sha256:95fd56811e6988170c229aa5cdd8c57b2d348e668e9fec1189d221bf13d64c6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:12-jdk21-eclipse-temurin` - linux; amd64

```console
$ docker pull jetty@sha256:370b0d2a99f6c5430a957d3663ac3fef5db76bbd692a4ac5653cca797251439d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269817252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d6cdc7a5ef125108a8c147a03bee66aec0bc35b95a69464380478aec50bdd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Thu, 07 May 2026 23:59:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:52 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:00:00 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 17:55:41 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 02 Jun 2026 17:55:41 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 Jun 2026 17:55:41 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 Jun 2026 17:55:41 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 Jun 2026 17:55:41 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 17:55:41 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 02 Jun 2026 17:55:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 Jun 2026 17:55:41 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 02 Jun 2026 17:55:41 GMT
WORKDIR /var/lib/jetty
# Tue, 02 Jun 2026 17:55:41 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 02 Jun 2026 17:55:41 GMT
USER jetty
# Tue, 02 Jun 2026 17:55:41 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 17:55:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 17:55:41 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8afc73467c288c6b0c7675f4ac20e8720099f39423b003316a19ecc111cc99d`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 24.1 MB (24097774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfc2aa0ff4805a388461869c789db4b743b3be95b159f1b0ee0d1cdd1ae844b`  
		Last Modified: Fri, 08 May 2026 00:00:48 GMT  
		Size: 158.2 MB (158171782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d45b0db0526b1b5acd7c6be9904e40d3c6d17ce2f4780c8c857ca8ca3128b8f`  
		Last Modified: Fri, 08 May 2026 00:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4245225757129cc521c360daa799b6ecafc22586f5852deadeb460a867729d`  
		Last Modified: Fri, 08 May 2026 00:00:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e548b633832ac58c880d4e6a7c79a48b784a5fe5ccbaea5d34e650c36bf3429f`  
		Last Modified: Tue, 02 Jun 2026 17:55:55 GMT  
		Size: 46.0 MB (45988133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74baa53f4179ae65df7bc061b74f8f017fd0104266c47d022b9d22e465e693e0`  
		Last Modified: Tue, 02 Jun 2026 17:55:53 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:ab32a594c5e89d890c33d271bec3469e1e27283910947a452b70d82bb5d54256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5700126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f011cc3e5e9304b52b0f31e085d184afe76218ccb874de481d759b8e997e8eb1`

```dockerfile
```

-	Layers:
	-	`sha256:ba603f8607b2a463dffcb22b4e3acefa684d979e44e2b9cb07ed40eac2e46c02`  
		Last Modified: Tue, 02 Jun 2026 17:55:54 GMT  
		Size: 5.7 MB (5677731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032e9c4f7b52efcad9760ef983a01f29aaeaf96f6b25ed960c41d554f89580f9`  
		Last Modified: Tue, 02 Jun 2026 17:55:53 GMT  
		Size: 22.4 KB (22395 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:12-jdk21-eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2deaa33fb29df032af1087ccca82938422aa5bd4ee5cdc660b000389495f8fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267163499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3575b82832cd6b3dd7224e1a4c4f9e084cd0000eb3a6fa48622d8004b7eb94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Thu, 07 May 2026 23:59:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:29 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:37 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 17:55:27 GMT
ENV JETTY_VERSION=12.1.10
# Tue, 02 Jun 2026 17:55:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 02 Jun 2026 17:55:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 02 Jun 2026 17:55:27 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 02 Jun 2026 17:55:27 GMT
ENV PATH=/usr/local/jetty/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 17:55:27 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/12.1.10/jetty-home-12.1.10.tar.gz
# Tue, 02 Jun 2026 17:55:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Tue, 02 Jun 2026 17:55:27 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg2 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	gpgconf --kill all ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Tue, 02 Jun 2026 17:55:28 GMT
WORKDIR /var/lib/jetty
# Tue, 02 Jun 2026 17:55:28 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Tue, 02 Jun 2026 17:55:28 GMT
USER jetty
# Tue, 02 Jun 2026 17:55:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 02 Jun 2026 17:55:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 17:55:28 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8b196d77d6a5bee5c7460c36b2dff891d15bfa5759d3b0ac088821412b696`  
		Last Modified: Thu, 07 May 2026 23:59:59 GMT  
		Size: 24.0 MB (23967737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052c69b546aa91a10006cc63cdae8549e35cf97072a4e8de735cd2e882849368`  
		Last Modified: Fri, 08 May 2026 00:00:02 GMT  
		Size: 156.5 MB (156473500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b1bd76e1150aa5cf3ade8362b362f71257889c7a8c253dab6945cb9913cfd`  
		Last Modified: Thu, 07 May 2026 23:59:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab6b91d002c02ca59b58ea550b7a544ffbed83a25633683cd47624257a86729`  
		Last Modified: Thu, 07 May 2026 23:59:58 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a8263cd88cf284543e65140d44fccca619e722542eab2d314708c416e5ea4d`  
		Last Modified: Tue, 02 Jun 2026 17:55:43 GMT  
		Size: 46.0 MB (45988604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dd6a31ec7e0158e4afdd1f9b623e094bda3f1fc7bf6f5e57847c380d67bec7`  
		Last Modified: Tue, 02 Jun 2026 17:55:42 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:12-jdk21-eclipse-temurin` - unknown; unknown

```console
$ docker pull jetty@sha256:b9b6f7416e220d68fc592e4719e96253928a4b198593b2efe9e8f535d9f152ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95556ff91f94bec91167d912ac87a872a0ef0fd428d22b2287bb40b7dbc3f0fb`

```dockerfile
```

-	Layers:
	-	`sha256:d32e8cfc6bf6d8bfe824d1858dfa744814a0b9e5f01c68704bc7ca606a6f0231`  
		Last Modified: Tue, 02 Jun 2026 17:55:42 GMT  
		Size: 5.9 MB (5865159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c053498c6d798926919fcdeed829efe08704fcf9df063844c16937b11484a9`  
		Last Modified: Tue, 02 Jun 2026 17:55:42 GMT  
		Size: 22.5 KB (22535 bytes)  
		MIME: application/vnd.in-toto+json
