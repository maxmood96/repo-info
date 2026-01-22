## `jetty:9-jdk21-alpine-amazoncorretto`

```console
$ docker pull jetty@sha256:a2bca8ce0703a7455570a439b923281acefd6e2a0b80ae13b6dc38aadd052b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; amd64

```console
$ docker pull jetty@sha256:c2a9dfdff89b2c35e8005a96bc161d0d258d3b2b6e92add0dba6b6dfb861290e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184888148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ecbb61f29fa605f9b34ddbf7bcbc3324c574f787e148243b920b5befe04fed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:15 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:15 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:18:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:18:34 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:18:34 GMT
USER jetty
# Wed, 21 Jan 2026 19:18:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:18:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:18:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3b5bdb09ad91d86c575799ac71f0f8e4cf37a35be2c5430890f6cad8a53919`  
		Last Modified: Wed, 21 Jan 2026 19:19:42 GMT  
		Size: 161.6 MB (161590231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd96d8fb8a3c5eea91981b06239cf6e7e71a94e98160c0b1b3ffb060aacc4556`  
		Last Modified: Wed, 21 Jan 2026 19:18:43 GMT  
		Size: 19.4 MB (19435937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f85410d4ac01fa0c160bf16f685c26837aac9291843f9525b61cb922aef4e46`  
		Last Modified: Wed, 21 Jan 2026 19:18:39 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:8a32625e453991965ab595a62cce6c56a8477d744936d4692ea53d9eb416e925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.5 KB (826481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6164ed0ac3609423adbf2aa5138c23a0f2ef89c0e1c6ca103dc88c4c05cf7d98`

```dockerfile
```

-	Layers:
	-	`sha256:4d4d6771c4d08bcbac7888dde2c66dc8e154b351b96ba7de83116bcd33879cd0`  
		Last Modified: Wed, 21 Jan 2026 19:18:43 GMT  
		Size: 809.4 KB (809375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cbd148d409e24ee21783932a7f11e748ad9d58c525d1422ab1b9985fa48c85d`  
		Last Modified: Wed, 21 Jan 2026 21:22:39 GMT  
		Size: 17.1 KB (17106 bytes)  
		MIME: application/vnd.in-toto+json

### `jetty:9-jdk21-alpine-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:7e894be704783b688fbc3f9252478528b08d24bd93c5475c07defe6469f8929a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183148158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5f0abf70e483e77fb89ba3b7ae429307da92dbca3153e4282c89685dbda157`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:33 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:33 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:33 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_VERSION=9.4.58.v20250814
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.58.v20250814/jetty-home-9.4.58.v20250814.tar.gz
# Wed, 21 Jan 2026 19:18:34 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	F254B35617DC255D9344BCFA873A8E86B4372146 	E22488CC94F63E3FC928536C4241C08270D999C3
# Wed, 21 Jan 2026 19:18:34 GMT
RUN set -xe ; 	mkdir -p $TMPDIR ; 	apk add --no-cache gnupg curl ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	case "$JETTY_VERSION" in 		"12."*) START_MODULES="server,http,ext,resources" ;; 		*) START_MODULES="server,http,deploy,ext,resources,jsp,jstl,websocket" ;; 	esac ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="$START_MODULES" ; 	addgroup -S jetty && adduser -h $JETTY_BASE -S jetty -G jetty; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	gpgconf --kill all ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ; # buildkit
# Wed, 21 Jan 2026 19:18:34 GMT
WORKDIR /var/lib/jetty
# Wed, 21 Jan 2026 19:18:34 GMT
COPY docker-entrypoint.sh generate-jetty-start.sh / # buildkit
# Wed, 21 Jan 2026 19:18:34 GMT
USER jetty
# Wed, 21 Jan 2026 19:18:34 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 21 Jan 2026 19:18:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Jan 2026 19:18:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed197f84715ef0ef979d302a0da27da3341c03c36879e415591cea9dc0bdf176`  
		Last Modified: Wed, 21 Jan 2026 19:18:25 GMT  
		Size: 159.6 MB (159615717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9471e9937580a5f089ad94b782223dd9573e65f06fb287e3e80dff6d20cae4`  
		Last Modified: Wed, 21 Jan 2026 19:18:43 GMT  
		Size: 19.3 MB (19334825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a5ab6cca3714439efda553298ca523448ddcec937ed656d126eb5aa81a2be7`  
		Last Modified: Wed, 21 Jan 2026 19:18:57 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `jetty:9-jdk21-alpine-amazoncorretto` - unknown; unknown

```console
$ docker pull jetty@sha256:c887d282620f4e8279952866bdf12150de037981f424568cbd75d878369c9d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.3 KB (825330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe8886f7a4a6ae10a1c11c950e7b5960b583b92d5dc5b7ef081a2af99f1700d`

```dockerfile
```

-	Layers:
	-	`sha256:6e0ba2c288aa1bf48eddf30495b0117e9ef8c35618f69ad5942a819730d4bbe0`  
		Last Modified: Wed, 21 Jan 2026 19:18:43 GMT  
		Size: 808.1 KB (808132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad848b170be20d9f5b49a0ea545a778006c9d38d99e9da94701c6cd659ba1e7`  
		Last Modified: Wed, 21 Jan 2026 19:18:42 GMT  
		Size: 17.2 KB (17198 bytes)  
		MIME: application/vnd.in-toto+json
