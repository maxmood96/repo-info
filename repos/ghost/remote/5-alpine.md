## `ghost:5-alpine`

```console
$ docker pull ghost@sha256:76332b92add671d2f8a7a79b319ec257bec473d66447f370f3ad8d977ce5361a
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

### `ghost:5-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:8d98fbffae91a6fc95ca8fb9e7a79686b5473c36b2900cea589d7b80b9bf0b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146809800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0bacc67b1d206a2954d0309a42bea820647ed93a5f674209e3ed827f1f62c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 23:05:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 23:05:18 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
CMD ["node"]
# Thu, 12 Dec 2024 18:06:53 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV NODE_ENV=production
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_VERSION=5.104.2
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Dec 2024 18:06:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:06:53 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 12 Dec 2024 18:06:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6f657bab0c137ad8a7930532dbd7c53338023e828890090a4070f47a2ed65d`  
		Last Modified: Mon, 18 Nov 2024 15:04:47 GMT  
		Size: 40.1 MB (40088838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f477ea663f1c2a017b6f95e743b5ad72f8ff8bf861b0759a86ba1985f706308f`  
		Last Modified: Mon, 18 Nov 2024 15:04:46 GMT  
		Size: 1.4 MB (1386284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c47a581c29baa57713ee0da7af754f3994227b64949cb5e9e4dbbc2108c6cd`  
		Last Modified: Mon, 18 Nov 2024 15:04:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfbed8e321cb71a6c79f522985a02665058c15cf19b1ba3c5f4a0ddf31654b2`  
		Last Modified: Thu, 12 Dec 2024 22:37:11 GMT  
		Size: 775.7 KB (775730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be00df09f51803036aa8f94244e8f7e29b7f918509d1f656c73cac1a9ebe0a79`  
		Last Modified: Thu, 12 Dec 2024 22:37:10 GMT  
		Size: 1.1 MB (1120709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baf809545fd1b2e908305e2fa6c247c3f51e975cd922f1ac5580eb527db8764`  
		Last Modified: Thu, 12 Dec 2024 22:37:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de53d6dd8e3c22d1f13fe6cf5e9cafa21a7b903a66cb74006d0d3321f1d5747f`  
		Last Modified: Thu, 12 Dec 2024 22:37:11 GMT  
		Size: 10.9 MB (10927976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be3974a5b7c51e6cbe07d04665705c493acde6662bcd701a9cd487b2cb835f8`  
		Last Modified: Thu, 12 Dec 2024 22:37:12 GMT  
		Size: 88.9 MB (88885155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5e21a581c26fce9d5213a43657bb46695875be1640f064ef9c34abd947ba03`  
		Last Modified: Thu, 12 Dec 2024 22:37:11 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:74b33190679e004fc32cc552e730e239ed7b39ef796bd4d2a79f7309da66dabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309dadaa346d284af5200e8b4d39826d80f920988535ee2a2b97e471e9e8c1a5`

```dockerfile
```

-	Layers:
	-	`sha256:5639373989ef5d9c7ca564946661ae305ff1e59b40fd20c3631409c1fddeb1f8`  
		Last Modified: Thu, 12 Dec 2024 22:37:10 GMT  
		Size: 3.3 MB (3313922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4ca47799a560753d7343f5dc3f1d1a818806da24f7f96d33035f48550fd225`  
		Last Modified: Thu, 12 Dec 2024 22:37:10 GMT  
		Size: 32.3 KB (32281 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v6

```console
$ docker pull ghost@sha256:0107958861b93f5136575e50a2aef8ee662517b29127b559e462867ca7925a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153341562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3aa3ef6702be82370b1db4462ea102172c5bb24849fa345c6baad0aaa6d089`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 23:05:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 23:05:18 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
CMD ["node"]
# Thu, 12 Dec 2024 18:06:53 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV NODE_ENV=production
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_VERSION=5.104.2
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Dec 2024 18:06:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:06:53 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 12 Dec 2024 18:06:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465c02069250b7065dee7c23182fba5e8b747c0448ce2ead861fb8beba3edc3`  
		Last Modified: Mon, 18 Nov 2024 19:47:10 GMT  
		Size: 38.5 MB (38493622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0d67662595d218900e16ff8c38f87b9a6fae977864c9902e4ea6bcfa9b630d`  
		Last Modified: Mon, 18 Nov 2024 19:47:09 GMT  
		Size: 1.4 MB (1386257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72823afcb96fe19e33dfcb0e2df2b07da2e1907c13a6ad8e8bb777100ce7528`  
		Last Modified: Mon, 18 Nov 2024 19:47:08 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc4e2ee3447dd17df58b4a13425444defb78f1d64dc3b78f940417406b61e3`  
		Last Modified: Thu, 12 Dec 2024 23:09:09 GMT  
		Size: 766.6 KB (766610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aa3a4cfa42c12e3d08ab6c6938e0c4e6716edf1ea59269a201411084493f1e`  
		Last Modified: Thu, 12 Dec 2024 23:09:09 GMT  
		Size: 1.1 MB (1087816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b966e0b1467f0ad63a91c7705daddf235360ffdf684e3b712a34d558adfca4cd`  
		Last Modified: Thu, 12 Dec 2024 23:09:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da777d5a01531aafa829409dc43bae2707df2f5acfc152977f5f321620ec001d`  
		Last Modified: Thu, 12 Dec 2024 23:09:09 GMT  
		Size: 10.9 MB (10938887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c37783718b60378f28d58c25a5f1747311ae78e131dd3b70f4f6c1ba2d978c`  
		Last Modified: Thu, 12 Dec 2024 23:09:12 GMT  
		Size: 97.3 MB (97300581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22a801d4d1f5132a3b2f0e54639a48ef8ae53b0e47be74933156838500c35a8`  
		Last Modified: Thu, 12 Dec 2024 23:09:10 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:d1c3749d043301515c2485b54c2db57584f6fcf2a3f05c729d771855a5d3358c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac0c4a875604fe1426583eec8fddb156a73bc1caaeda9586a4399298bd2193`

```dockerfile
```

-	Layers:
	-	`sha256:d4203a325fe80e7ca07d86fed60c48be8e6dca28fbfd98b1de4e95daf76e9612`  
		Last Modified: Thu, 12 Dec 2024 23:09:08 GMT  
		Size: 32.2 KB (32194 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm variant v7

```console
$ docker pull ghost@sha256:7117be5aa23fb678750c563f38c298b4abdf0ccfe8d0a9b463f62c20c573deaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152184092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448c6d9fd4de888f1cf266940c6d3b9c971b0d2d751e9811011ca2481cbd8cf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 23:05:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 23:05:18 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
CMD ["node"]
# Thu, 12 Dec 2024 18:06:53 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV NODE_ENV=production
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_VERSION=5.104.2
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Dec 2024 18:06:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:06:53 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 12 Dec 2024 18:06:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f9530472ec755c495a6a6700f14dfdef8401e9517a4b85c6bbec992f004cf6`  
		Last Modified: Mon, 18 Nov 2024 20:16:54 GMT  
		Size: 38.0 MB (37995865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54323950fc027f6cf7c005c4426010ee2ba22470668f6a8b8c7f4daf33dc44d0`  
		Last Modified: Mon, 18 Nov 2024 20:16:53 GMT  
		Size: 1.4 MB (1386268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ac3ab1f81f4188acba1e55898694cbb4891f390070ba9c61e06ec81ad24def`  
		Last Modified: Mon, 18 Nov 2024 20:16:52 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bd162301fc96c2d4a326903ce778a27aabec84c4ed64defe346c28d0e980e5`  
		Last Modified: Fri, 13 Dec 2024 00:13:47 GMT  
		Size: 700.6 KB (700650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1533c0dea474b813fa95d69cb7c400973a9c11c91bae8dec92c96b797d118001`  
		Last Modified: Fri, 13 Dec 2024 00:13:47 GMT  
		Size: 1.1 MB (1087849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06ca917427d77bbf016004c848f7d92328e9692f78a4a4a847f985ce6719136`  
		Last Modified: Fri, 13 Dec 2024 00:13:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1b32a0c5f0082d3b823a82742d8b8d71684a3f1a8b7ed34015b13e19a1543`  
		Last Modified: Fri, 13 Dec 2024 00:13:48 GMT  
		Size: 10.9 MB (10930428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0691515ac999bf8a2fde4ed634c15a4c55d0766f87fcd6932641a6553b798df1`  
		Last Modified: Fri, 13 Dec 2024 00:13:51 GMT  
		Size: 97.0 MB (96986351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb659be434c8eb7630f5607a4f23022711a32a426a34c7fc1337e549c580368`  
		Last Modified: Fri, 13 Dec 2024 00:13:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:50981131c217d73a75c533529b91c7948c6098be2c44dbb43011e227cf5078fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3338364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4379e6f5625be6934521b784c79790532460f91954aff9a380d32b2bac0e40df`

```dockerfile
```

-	Layers:
	-	`sha256:fe3725366362ffc710ec20afb433e5fd2bfcc68098ba3957fb5d7c27ff372cb9`  
		Last Modified: Fri, 13 Dec 2024 00:13:47 GMT  
		Size: 3.3 MB (3305955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffe7e2058a17db56ee8ca42b8a89ffaf57ba0c3bcda5b3cc214718a6496136c`  
		Last Modified: Fri, 13 Dec 2024 00:13:47 GMT  
		Size: 32.4 KB (32409 bytes)  
		MIME: application/vnd.in-toto+json

### `ghost:5-alpine` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:c168664332f1e06481b884d51dfedc66102b05ef7b0081ff4a208f0b78eb4ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166834215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9bca235ab37ea5a9e99856ff5eb0b4aba6a6ec60ab21280d8cb265069e0a44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
ENV NODE_VERSION=18.20.5
# Fri, 15 Nov 2024 23:05:18 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="deaf95aceeb446d8861419884fc1d07c54e4a958e4d9b82d8fb9c8f1f7001535" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENV YARN_VERSION=1.22.22
# Fri, 15 Nov 2024 23:05:18 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Nov 2024 23:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Nov 2024 23:05:18 GMT
CMD ["node"]
# Thu, 12 Dec 2024 18:06:53 GMT
RUN apk add --no-cache 		bash # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (TODO remove in Ghost 6+) # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV NODE_ENV=production
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CLI_VERSION=1.26.1
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	npm install -g "ghost-cli@$GHOST_CLI_VERSION"; 	npm cache clean --force # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 12 Dec 2024 18:06:53 GMT
ENV GHOST_VERSION=5.104.2
# Thu, 12 Dec 2024 18:06:53 GMT
RUN set -eux; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		apkDel=; 		installCmd='gosu node ghost install "$GHOST_VERSION" --db mysql --dbhost mysql --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"'; 	if ! eval "$installCmd"; then 		virtual='.build-deps-ghost'; 		apkDel="$apkDel $virtual"; 		apk add --no-cache --virtual "$virtual" g++ linux-headers make python3; 		eval "$installCmd"; 	fi; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --no-prompt --ip '::' --port 2368 --url 'http://localhost:2368'; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 	chmod 1777 "$GHOST_CONTENT"; 		cd "$GHOST_INSTALL/current"; 	packages="$(node -p ' 		var ghost = require("./package.json"); 		var transform = require("./node_modules/@tryghost/image-transform/package.json"); 		[ 			"sharp@" + transform.optionalDependencies["sharp"], 			"sqlite3@" + ghost.optionalDependencies["sqlite3"], 		].join(" ") 	')"; 	if echo "$packages" | grep 'undefined'; then exit 1; fi; 	for package in $packages; do 		installCmd='gosu node yarn add "$package" --force'; 		if ! eval "$installCmd"; then 			virtualPackages='g++ make python3 py3-setuptools'; 			case "$package" in 				sharp@*) echo >&2 "sorry: libvips 8.12.1 in Alpine 3.15 is not new enough (8.12.2+) for sharp 0.30 😞"; continue ;; 			esac; 			virtual=".build-deps-${package%%@*}"; 			apkDel="$apkDel $virtual"; 			apk add --no-cache --virtual "$virtual" $virtualPackages; 						eval "$installCmd --build-from-source"; 		fi; 	done; 		if [ -n "$apkDel" ]; then 		apk del --no-network $apkDel; 	fi; 		gosu node yarn cache clean; 	gosu node npm cache clean --force; 	npm cache clean --force; 	rm -rv /tmp/yarn* /tmp/v8* # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
WORKDIR /var/lib/ghost
# Thu, 12 Dec 2024 18:06:53 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 12 Dec 2024 18:06:53 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 12 Dec 2024 18:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:06:53 GMT
EXPOSE map[2368/tcp:{}]
# Thu, 12 Dec 2024 18:06:53 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3488cb9db70902527d81898e2a7f4d11728544d7dd9db3328a866418accb9b0`  
		Last Modified: Mon, 18 Nov 2024 17:42:40 GMT  
		Size: 39.6 MB (39619200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24672547edfea5a1e6e28d83498ba598901d4d9d04da062e0fbde5ddf24bf9df`  
		Last Modified: Mon, 18 Nov 2024 17:42:38 GMT  
		Size: 1.4 MB (1386274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c4b655b5556f55ed9713b72d7be3538e4d21ab031213c969e3fc1868b8fb8c`  
		Last Modified: Mon, 18 Nov 2024 17:42:38 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02032701052ca20efeb22bdba9c1343cfb149ad7a0a2bea92090304af7d57ca3`  
		Last Modified: Tue, 10 Dec 2024 02:05:12 GMT  
		Size: 853.5 KB (853507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2695c472471fc718afb2929660503d90b93fba159da96d5a304c7641d22ded4`  
		Last Modified: Tue, 10 Dec 2024 02:05:12 GMT  
		Size: 1.1 MB (1051642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa43c890ff485bacaab81780ce7a1c6df576c351e6e1ede0ee78e37e452607e`  
		Last Modified: Tue, 10 Dec 2024 02:05:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e1995f279ca2668c7746a48ee6cda510bf7fff9c3ffc634cf5bff62e1be635`  
		Last Modified: Tue, 10 Dec 2024 02:05:12 GMT  
		Size: 10.9 MB (10929319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058cb10ae8dcbe107e102b49d048560c3ba3267424088d591876e763a47d8f65`  
		Last Modified: Fri, 13 Dec 2024 00:35:09 GMT  
		Size: 108.9 MB (108905354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff11ff2d17ce2c17410c742cfb10360d629f4e62fc7886b882d575d363db8d81`  
		Last Modified: Fri, 13 Dec 2024 00:35:06 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ghost:5-alpine` - unknown; unknown

```console
$ docker pull ghost@sha256:638ca1e77ed7fa90598d8eaac87a52ece0199e73b06be2ea7fc698df6846b98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abefc62076c14d018d31d76434e147d2444849990024c0879dabcdb435c35e0a`

```dockerfile
```

-	Layers:
	-	`sha256:64659d1a1ed64b06985b9875b8c7b645c2cc2c0ed8c298cff135eca99f64d372`  
		Last Modified: Fri, 13 Dec 2024 00:35:06 GMT  
		Size: 3.3 MB (3313978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb6d98682050e6a547a9f659c2e0d0059d017670a9e337212f9ca86badc3cfe`  
		Last Modified: Fri, 13 Dec 2024 00:35:06 GMT  
		Size: 32.4 KB (32448 bytes)  
		MIME: application/vnd.in-toto+json
