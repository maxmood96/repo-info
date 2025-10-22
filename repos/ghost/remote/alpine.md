## `ghost:alpine`

```console
$ docker pull ghost@sha256:4397cc7a8e5ade63a7cc5a49267cdf4f99da6c3136f133eb927d531faa985089
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:f64f12326c0b9a592f4cdd13342ec98a69c86d6eec5bce1fd1756815fe515a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196075800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65128d286954c395576e9f71c20c7710cd14cd996445f4e8aafd8d897de3abb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 04:06:16 GMT
ENV NODE_VERSION=22.21.0
# Tue, 21 Oct 2025 04:06:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b328e2cec3c7bd4d84656cee389dfd1fd5a96048c674c8e7d2b1dd9b0628da9d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 21 Oct 2025 04:06:16 GMT
ENV YARN_VERSION=1.22.22
# Tue, 21 Oct 2025 04:06:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 21 Oct 2025 04:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 04:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 04:06:16 GMT
CMD ["node"]
# Wed, 22 Oct 2025 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_VERSION=6.5.0
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 22 Oct 2025 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 22 Oct 2025 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Oct 2025 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 22 Oct 2025 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9682177f5dda1fd55072217f7077e1c680daaa4e23e02a3cb1274868a8aa082e`  
		Last Modified: Tue, 21 Oct 2025 20:18:36 GMT  
		Size: 51.6 MB (51554700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e910c7b62cc771efdec5776c0a1f50d1730a1c9c9acbdfb67c2de365f5e99d2e`  
		Last Modified: Tue, 21 Oct 2025 20:18:30 GMT  
		Size: 1.3 MB (1260579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9e06b66aaed551c8dd195ece4a1bb9a96da16cb8d4d6fc9321919008650303`  
		Last Modified: Tue, 21 Oct 2025 20:18:30 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9a7a473f9bbc43b5019041bae278085205f4ffab4cdb7ffd5aab4e7708327`  
		Last Modified: Wed, 22 Oct 2025 17:51:47 GMT  
		Size: 777.0 KB (777037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e92fc52af38eb171bb9b4d05741449b9c2ecf523c09b6980f253ea94253aa0`  
		Last Modified: Wed, 22 Oct 2025 17:51:47 GMT  
		Size: 923.4 KB (923433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40a70250ea6e270eebe151db8309da4bf856cec5475b0b785f1c6b1e82ead24`  
		Last Modified: Wed, 22 Oct 2025 17:51:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469340a0fd9aab04d91ccbdd9c90ed82458d66292b892cf3956d47280178d67`  
		Last Modified: Wed, 22 Oct 2025 17:51:48 GMT  
		Size: 11.7 MB (11660015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f664dbf2503dfe9ddfda0bd0c17259bf5e1a7f2c301f564314f3f66f7e1b64ec`  
		Last Modified: Wed, 22 Oct 2025 17:51:58 GMT  
		Size: 126.1 MB (126096384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6240823944fda773d79c7936864c0505ab5fb2aefdcced87d035db1a346f23`  
		Last Modified: Wed, 22 Oct 2025 17:51:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:956b0976bcbff1fae03d49b8a82f9901c429de1802de35a1017f9410088aba4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abd9453cb8b7163b2f7b5fe76310e8bb813b9049cd108d970fc719eb84a850a`

```dockerfile
```

-	Layers:
	-	`sha256:c2e27027bb2dd9e01e6f6e67862c5808648dd4215e2d53f4530c92290c4fe6c5`  
		Last Modified: Wed, 22 Oct 2025 18:45:37 GMT  
		Size: 3.3 MB (3340849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776484eff23cebdded665aa3894484d545a821d61d98af916bbec033968937d2`  
		Last Modified: Wed, 22 Oct 2025 18:45:37 GMT  
		Size: 32.6 KB (32554 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:e32e5e725630a0b6a4fd47c778032339dc88c939a615db2cee2bff5341051a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194784971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9633d9d9462d1aa3d5ad0aeabb453b7f3510174c954c344667300cb7bf6642`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_VERSION=22.21.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b328e2cec3c7bd4d84656cee389dfd1fd5a96048c674c8e7d2b1dd9b0628da9d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV YARN_VERSION=1.22.22
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a81391dc91bee5b5920075a9ed1c30b325b5eb3e42ccfdf6686a20ba18f31d`  
		Last Modified: Tue, 21 Oct 2025 19:37:26 GMT  
		Size: 49.2 MB (49230806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23132e583cc416495100c8a80f1c06f9ce56bac9d29fae6568a99127a17fb90`  
		Last Modified: Tue, 21 Oct 2025 19:37:24 GMT  
		Size: 1.3 MB (1260561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fb583891d80b3351b57f39f08043e184e9671421a7f60f75537908b0ad8419`  
		Last Modified: Tue, 21 Oct 2025 19:37:23 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a0974a07b10fb199844780cb48355c5325d9502d7ec915648e326895455d5`  
		Last Modified: Tue, 21 Oct 2025 20:07:40 GMT  
		Size: 766.1 KB (766084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f35803f3928889ea9b76f6e373b07e4ef353f4723f46cbcde0a00a76e37c46`  
		Last Modified: Tue, 21 Oct 2025 20:07:40 GMT  
		Size: 889.1 KB (889103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f905b7a29815d9aa188357eb14329113e4a345cca17466d4e148c575a2f9ea`  
		Last Modified: Tue, 21 Oct 2025 20:07:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53617ac3b7debe4c32904336317af63492e2b20b9d0b576d15aaf68efe81fa3`  
		Last Modified: Tue, 21 Oct 2025 20:07:42 GMT  
		Size: 11.7 MB (11665574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9999bdd3f4e807cc9e965638c08d12740140b1688ebc6547751b3866491d9`  
		Last Modified: Tue, 21 Oct 2025 20:07:54 GMT  
		Size: 127.5 MB (127467580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a6fab4fddd7a133828088722912615daa5e846d0fbea67fe992d7bc2a10ff`  
		Last Modified: Tue, 21 Oct 2025 20:07:40 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:ae576cd5944661730eb6c1e437cfabb6cd9930d3f7f1526ca2a579f09f7907a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ab3c9419efecef894a836812d52dc1a8a37421d1cda4241cd4439a1b998de`

```dockerfile
```

-	Layers:
	-	`sha256:7557dd55712e7f6047d28543af4d93304caadcc734732e5be21e714ebe2d1610`  
		Last Modified: Tue, 21 Oct 2025 21:46:19 GMT  
		Size: 32.5 KB (32471 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:225fcd18a571175648ebd2d861fe573a5cfeddf76b124b8429fb6bfaeddd0593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193430614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a262352b88da03f64beebe3b9d5f33787a4e1d7ef7870f0199019158fee1d31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_VERSION=22.21.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b328e2cec3c7bd4d84656cee389dfd1fd5a96048c674c8e7d2b1dd9b0628da9d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV YARN_VERSION=1.22.22
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node"]
# Fri, 17 Oct 2025 18:05:45 GMT
RUN apk add --no-cache 		bash # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV NODE_ENV=production
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 17 Oct 2025 18:05:45 GMT
ENV GHOST_VERSION=6.4.0
# Fri, 17 Oct 2025 18:05:45 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
WORKDIR /var/lib/ghost
# Fri, 17 Oct 2025 18:05:45 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 17 Oct 2025 18:05:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Oct 2025 18:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Oct 2025 18:05:45 GMT
EXPOSE map[2368/tcp:{}]
# Fri, 17 Oct 2025 18:05:45 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f70225b8a1d3b47e12e1cf00bec84606b4cbc698ec5960d67669064b3cf14c`  
		Last Modified: Tue, 21 Oct 2025 19:43:27 GMT  
		Size: 48.5 MB (48529437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d4faf93cda188d03c134224c7de71331fea3d245fae322f450507cccfd19b`  
		Last Modified: Tue, 21 Oct 2025 19:43:23 GMT  
		Size: 1.3 MB (1260547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33a9be3c3e50b78699a185455c2e10968405466b4825cf070075740f09cf53c`  
		Last Modified: Tue, 21 Oct 2025 19:43:22 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e54363765ac9a870156a38c8527c193e14c1d9653ef67c69eb3ecd70d002d31`  
		Last Modified: Tue, 21 Oct 2025 21:18:17 GMT  
		Size: 701.5 KB (701475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a0194d581070493b2ccdb369e1d873f12ca53dd58723ee1023f47093a1fdac`  
		Last Modified: Tue, 21 Oct 2025 21:18:20 GMT  
		Size: 889.1 KB (889093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95756d5b968e9345d7082e198d8d2d3e60fbb9e24aef2bf80cc1879cfa1f629b`  
		Last Modified: Tue, 21 Oct 2025 21:18:23 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478efebb7727b0b47f99c4ae065ab3b412ebf9ec69248c04292046e7a7125349`  
		Last Modified: Wed, 22 Oct 2025 01:07:02 GMT  
		Size: 11.7 MB (11659416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0d29452ebbf67aaf3b4f037a7e7ead3bfe46528d804a8786938b8d36bd2565`  
		Last Modified: Wed, 22 Oct 2025 01:07:12 GMT  
		Size: 127.2 MB (127167907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa7b7172c172bdd5010b1aa57f82ee1b0aafa1564c9c815fef127e5ce8f33e2`  
		Last Modified: Tue, 21 Oct 2025 21:18:30 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:fb4b6083ab455aafc71c96f8e8d7d6ba1fc21d1173555fb745395207bc6a3ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e718fdad52b2d2e5a6b6f4f421c632ac87e5bfc86baed10478d0674867b184`

```dockerfile
```

-	Layers:
	-	`sha256:4aed52ce596a777280ec5407a7f3f574c08b2b0940dee3c8fd94f84bf3945fba`  
		Last Modified: Tue, 21 Oct 2025 21:46:22 GMT  
		Size: 3.3 MB (3337874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab9fcde636dda164221064fbb723271d071b59a99e954fd259733af64f07095`  
		Last Modified: Tue, 21 Oct 2025 21:46:23 GMT  
		Size: 32.7 KB (32686 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:2946544392dda0a2f26d542d4cce606dc35a54f6ffc7a4f94c7c156d68212290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206950866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3160a418d3c08d55febfde53e566ed9855b386300fa35810c73a64d3e5e31ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 04:06:16 GMT
ENV NODE_VERSION=22.21.0
# Tue, 21 Oct 2025 04:06:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="b328e2cec3c7bd4d84656cee389dfd1fd5a96048c674c8e7d2b1dd9b0628da9d" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       5BE8A3F6C8A5C01D106C0AD820B1A390B168D356       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 21 Oct 2025 04:06:16 GMT
ENV YARN_VERSION=1.22.22
# Tue, 21 Oct 2025 04:06:16 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 21 Oct 2025 04:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 04:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 04:06:16 GMT
CMD ["node"]
# Wed, 22 Oct 2025 14:19:12 GMT
RUN apk add --no-cache 		bash # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENV NODE_ENV=production
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Wed, 22 Oct 2025 14:19:12 GMT
ENV GHOST_VERSION=6.5.0
# Wed, 22 Oct 2025 14:19:12 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
WORKDIR /var/lib/ghost
# Wed, 22 Oct 2025 14:19:12 GMT
VOLUME [/var/lib/ghost/content]
# Wed, 22 Oct 2025 14:19:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 22 Oct 2025 14:19:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Oct 2025 14:19:12 GMT
EXPOSE map[2368/tcp:{}]
# Wed, 22 Oct 2025 14:19:12 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a110d1eff85dcd1174fbd88a54b5dcfe3e1e9457def04b99a5c8464eb4974a8b`  
		Last Modified: Tue, 21 Oct 2025 19:41:36 GMT  
		Size: 51.3 MB (51254323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1494ccb64b72be65db13e78aad33d614e4078f672c3399db06cde39a75322619`  
		Last Modified: Tue, 21 Oct 2025 19:41:32 GMT  
		Size: 1.3 MB (1260566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c712bb59ac9f218f1661be129544be352c4c1f3b385441cb58383d0248eace15`  
		Last Modified: Tue, 21 Oct 2025 19:41:31 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c616b359a68dfc2e41fce5e670b16f811d9fb82d5324e3f61ac62ffac7a92`  
		Last Modified: Wed, 22 Oct 2025 17:53:15 GMT  
		Size: 838.6 KB (838573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335fe9eb62e72b24804ce5c4c77066689d5adefd79a311b6eee96a6ed6f5cb18`  
		Last Modified: Wed, 22 Oct 2025 17:53:15 GMT  
		Size: 876.4 KB (876367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b331cd5af35b5be94ce30603ac37c8f0c8de8e48a00c0f325f8c09b916c86ba3`  
		Last Modified: Wed, 22 Oct 2025 17:53:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053bc5ce31e0f82e84c172e45b006c02cb19a8f9110d3c055f51fda1384d17e1`  
		Last Modified: Wed, 22 Oct 2025 17:53:17 GMT  
		Size: 11.7 MB (11664109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9368c1be39d6697f7d672910842fadd6603da11a925fd7c25a3ad2644f47552`  
		Last Modified: Wed, 22 Oct 2025 18:46:01 GMT  
		Size: 136.9 MB (136917665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69082c2cb23c91e77520ac529b3d48993e72aabf57ac00da7c60b23a86b8347`  
		Last Modified: Wed, 22 Oct 2025 17:53:14 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:7990437eb1978e1345668edfad3797c2061262abbc9675dcacb7a2257a761efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94df822e6a417e890d79c4c6e70b63fcdad626b215ac7554905baea8857cd096`

```dockerfile
```

-	Layers:
	-	`sha256:1f6a06811983765ea8748caa9d34c380f6ce05ec67c80e7d95be13662a4d459a`  
		Last Modified: Wed, 22 Oct 2025 18:45:44 GMT  
		Size: 3.3 MB (3340957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f5df1980526e05e637d753f00bce0d7c388c113e3d58c24fa7196cc6b67c8f`  
		Last Modified: Wed, 22 Oct 2025 18:45:46 GMT  
		Size: 32.7 KB (32718 bytes)  
		MIME: application/vnd.in-toto+json
