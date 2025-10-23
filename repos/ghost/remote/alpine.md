## `ghost:alpine`

```console
$ docker pull ghost@sha256:4d7db6e61d10e4b23b9ce462e8cdebc689168a6ab4fa84f12af8ba52fd532e9f
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
$ docker pull ghost@sha256:6e769cc7e8e5aabd1745ce151b312950b9af22571143ea5d6e5220e33ff8a4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194782993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4444e02af033f0c80a6f247dc9c08598eb0b9f1a84abe0a2f116a872a7c927ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
# Thu, 23 Oct 2025 14:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV NODE_ENV=production
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_VERSION=6.5.1
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
WORKDIR /var/lib/ghost
# Thu, 23 Oct 2025 14:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 23 Oct 2025 14:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 14:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 23 Oct 2025 14:19:13 GMT
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
	-	`sha256:fbb7aa3a56c3007d041ad4da56045916c4f5c5749cf0d2fa4491c5182cbcf355`  
		Last Modified: Thu, 23 Oct 2025 21:34:30 GMT  
		Size: 766.1 KB (766088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753bf97ae253f8e9a9c4c21003aa358c621be3bd3ec5c85140f85f79b1e298b9`  
		Last Modified: Thu, 23 Oct 2025 21:34:30 GMT  
		Size: 889.1 KB (889104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a283e03f4e3d970e78f8e9bed8da0d53aac9db6a4fc820d3451ecf507f3ed6a`  
		Last Modified: Thu, 23 Oct 2025 21:34:30 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5d71efe5835babc6c67555288f3a250e2f25cc41da2d32766d089155add629`  
		Last Modified: Thu, 23 Oct 2025 21:34:31 GMT  
		Size: 11.7 MB (11665287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bc620fafe4b5ad7677c8321723ad0903bd4821242c1b84380718d1b6a5cf0`  
		Last Modified: Thu, 23 Oct 2025 21:34:44 GMT  
		Size: 127.5 MB (127465875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017361659a605f65bbb55b31ed482cc7aa0af935d57f4c7e7a260f92d2659151`  
		Last Modified: Thu, 23 Oct 2025 21:34:30 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:84ef82c877c6bc512bacb10b91df4a696305f1782a3bc4ba2de0937f05e9e728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 KB (32471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a66516bb1614fc3d9e3428f0b72aa3cc866ec996f96274bc6a75119cf8ac106`

```dockerfile
```

-	Layers:
	-	`sha256:c96ffd5ab51150369c580106c859eb89f0fdee775de7aeb49b34aee33119b1fe`  
		Last Modified: Thu, 23 Oct 2025 21:45:48 GMT  
		Size: 32.5 KB (32471 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:4b46d247a18c477bbc00d479344965608c443ae4519af42d8728ac9099e2d32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193429811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870aa65c979740b4390250d57c92dc378eb62189b2d726204dcf298d3edfa29c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
# Thu, 23 Oct 2025 14:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV NODE_ENV=production
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_VERSION=6.5.1
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
WORKDIR /var/lib/ghost
# Thu, 23 Oct 2025 14:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 23 Oct 2025 14:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 14:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 23 Oct 2025 14:19:13 GMT
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
	-	`sha256:b3342ef11961cfca255664d854a662137c7d153feec73af13eda7b060669d1bc`  
		Last Modified: Thu, 23 Oct 2025 21:34:45 GMT  
		Size: 701.5 KB (701476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a39ac6b5e4604207bf995b2a0718e8ceee41f8a12d0e7a7ab76f0f7a91301c6`  
		Last Modified: Thu, 23 Oct 2025 21:34:45 GMT  
		Size: 889.1 KB (889099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ef3b8ae54ffeb02c2b43d0b896094e85cfb0a22019430378648073f082b9c`  
		Last Modified: Thu, 23 Oct 2025 21:34:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355746ae7b450d0c0bdc9891fed1ef657a7d3486409dd7015bc1aa234525eb82`  
		Last Modified: Thu, 23 Oct 2025 21:34:46 GMT  
		Size: 11.7 MB (11658999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446397ed3323bb85f35a30be85cca34419701ad575d21c66292a088c788742c7`  
		Last Modified: Thu, 23 Oct 2025 21:34:59 GMT  
		Size: 127.2 MB (127167511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5d6d3303e2682336eec5a61a0dfb93b17db7692ab78a1945d1c6da732b6f05`  
		Last Modified: Thu, 23 Oct 2025 21:34:45 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:5213f4569b578693054e163ba21deb5a70804f7cee020a7cafaf588884c847a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43939baefbccee53bbfe816b49f89c942ed83a04cc5ea8211a9a995c345efacc`

```dockerfile
```

-	Layers:
	-	`sha256:5604f08b85e2c0240d0c0f1c9e42757b4c444c0e7bac90f2630fc0d507ffc0bb`  
		Last Modified: Thu, 23 Oct 2025 21:45:52 GMT  
		Size: 3.3 MB (3337874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be793e7ff5cbc02b9e7f7a382b6aa261ab5aeb9c012e67d896cc80a86209a0c`  
		Last Modified: Thu, 23 Oct 2025 21:45:52 GMT  
		Size: 32.7 KB (32686 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:be04940d8715e94fee2c9ef8d548ffd656731f81a00e402994b50de91cd2e2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206949927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c166a3ec7519719de6ff32a99a6b9c9618f3289cb57c39e50e42acffee9314`
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
# Thu, 23 Oct 2025 14:19:13 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV NODE_ENV=production
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_CLI_VERSION=1.28.3
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 23 Oct 2025 14:19:13 GMT
ENV GHOST_VERSION=6.5.1
# Thu, 23 Oct 2025 14:19:13 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	case "$GHOST_VERSION" in *-alpha* | *-beta* | *-rc*) installCmd="$installCmd --channel next" ;; esac; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
WORKDIR /var/lib/ghost
# Thu, 23 Oct 2025 14:19:13 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 23 Oct 2025 14:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 23 Oct 2025 14:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 14:19:13 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 23 Oct 2025 14:19:13 GMT
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
	-	`sha256:862f7e51ea5073e2cea79d5016fadf1773e1ea640f90ee6928c9a8cfd90bc4a4`  
		Last Modified: Thu, 23 Oct 2025 21:32:16 GMT  
		Size: 838.6 KB (838572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d32bf4051850bd687c12ed4113da26b6e1975c03eecd3bb0ec61b721e084f89`  
		Last Modified: Thu, 23 Oct 2025 21:32:16 GMT  
		Size: 876.4 KB (876363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a10fb7662ff04cdefd0a5eb870be3f5346a02a3840b06a115f6855be7fc392a`  
		Last Modified: Thu, 23 Oct 2025 21:32:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc49ae4bbf6be18983e5855e24055919cb84f7971bfc0e5e0a70faa04c9e27a6`  
		Last Modified: Thu, 23 Oct 2025 21:32:16 GMT  
		Size: 11.7 MB (11664638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe66a757ab9e84e9b4d6a045bd8f980c9c7d1c6b60de348b036d8409e1b8d89a`  
		Last Modified: Thu, 23 Oct 2025 21:46:11 GMT  
		Size: 136.9 MB (136916204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a54ab66bfc478a8e03f5337d5a15ee704e1c3ac21955f24ef1e1f03e9523e20`  
		Last Modified: Thu, 23 Oct 2025 21:32:16 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:59a847c9829c8ae6be6928db5676af3849e93def526cffdb6a6ff63c9644bcbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3373674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248b01f56d29ec4fe50a9639e9aa28c328145753495015f6f5a83df90d698453`

```dockerfile
```

-	Layers:
	-	`sha256:c93f3804e231d69902c71fe2997ceaf2ac8329e987345522d189fbab6ef1bb64`  
		Last Modified: Thu, 23 Oct 2025 21:45:57 GMT  
		Size: 3.3 MB (3340957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39dde4126fc0c56852722652c9c77e683f9a5c2e216c0fa7aca2a6d7b9c4edb`  
		Last Modified: Thu, 23 Oct 2025 21:45:57 GMT  
		Size: 32.7 KB (32717 bytes)  
		MIME: application/vnd.in-toto+json
