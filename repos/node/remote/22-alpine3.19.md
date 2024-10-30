## `node:22-alpine3.19`

```console
$ docker pull node@sha256:c3de5c419814674dfa127bc9df48aa1899e7f9cf6913b79da6eee31a38c0120d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:22-alpine3.19` - linux; amd64

```console
$ docker pull node@sha256:ec27f2ae7fa2d37dda976858a900fe80ebc9aff15e885bd5d113acd93e985615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54050618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d81bb0ba90dffc57923ac45847725a6fad6245a5379818581bb289685a79c36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
ENV NODE_VERSION=22.11.0
# Tue, 29 Oct 2024 20:39:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="95e9a410b7ce732705493cd44496c8e77ccb11516c75c2ef794f19a9943d178c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENV YARN_VERSION=1.22.22
# Tue, 29 Oct 2024 20:39:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2771ee72dd8c5e30e21ec9a453a8dba72b309d43d4e690dd110e3cd508e3bd`  
		Last Modified: Tue, 29 Oct 2024 21:57:41 GMT  
		Size: 49.2 MB (49243242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26850589665abd4869a5c2281ee7e87e7d3fe194a732f1f87e4b657b857136df`  
		Last Modified: Tue, 29 Oct 2024 21:57:40 GMT  
		Size: 1.4 MB (1387223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255d74c15f37ef5b1804216bf93c7df9246548fe1d702ac708c077dc1d335ffd`  
		Last Modified: Tue, 29 Oct 2024 21:57:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:c253e58315d2d3221f927c7163cdecea1bf41113538e23f6ce165aa4f9bd7f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.5 KB (439545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f972f4293ddd8a491386a53aa1b1cfb00e42070011df3a85f8206cc0467c1ad`

```dockerfile
```

-	Layers:
	-	`sha256:76d676c7998675285cdd7ece6fa3db823736f9aedbdfad18f2ab8c57938b88d9`  
		Last Modified: Tue, 29 Oct 2024 21:57:40 GMT  
		Size: 415.9 KB (415934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934cc2be5f90eb52e106acde879d40106e158db6669a9795e7af0cff6910cce3`  
		Last Modified: Tue, 29 Oct 2024 21:57:40 GMT  
		Size: 23.6 KB (23611 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; arm variant v6

```console
$ docker pull node@sha256:f56b38d0de588c19a6467c57598b0a3dd2a02c1e5246d75b660b55f8946516c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51950367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4985b9bd02b029d38a391d98f9719d31a5a2ec77a4bf1fbb70caf542acd1c8f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 02:51:22 GMT
ENV NODE_VERSION=22.10.0
# Thu, 17 Oct 2024 02:51:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="a964af3cbb33c2704739f792e2825659a93a2787253483350051bd48f6f3e8d9" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       4ED778F539E3634C779C87C6D7062848A1AB005C       141F07595B7B3FFE74309A937405533BE57C7D57       74F12602B6F1C4E913FAA37AD3A89613643B6201       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Thu, 17 Oct 2024 02:51:22 GMT
ENV YARN_VERSION=1.22.22
# Thu, 17 Oct 2024 02:51:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 17 Oct 2024 02:51:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 02:51:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 02:51:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ebead091c3eee0536a61007517d3f4fc97030e657b750b9b4dc09c78777c7`  
		Last Modified: Thu, 17 Oct 2024 22:03:56 GMT  
		Size: 47.4 MB (47386306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc400d67f451549bfe00e6cc4f1334daf5c77d2f426655ca2bfc367856be10f2`  
		Last Modified: Thu, 17 Oct 2024 22:03:54 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af15a3eb17b41060f3991589710f9edccb383714d685a0bc9f7fc01b36cec7da`  
		Last Modified: Thu, 17 Oct 2024 22:03:54 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:4342160f30fdebf5eebed7e9f9bdd0da1864cf5189033962c830e27cf61a191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 KB (23314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e850d85f488a986acd4ecc25b37eab3bb7f4ee3f164d5ff219ad4d53e6d1d6`

```dockerfile
```

-	Layers:
	-	`sha256:a92822fe9401841e0b48413e32bfccab2844b72901de2df804488ecb5aa874a1`  
		Last Modified: Thu, 17 Oct 2024 22:03:54 GMT  
		Size: 23.3 KB (23314 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; arm variant v7

```console
$ docker pull node@sha256:2711c93658fadae6b37d1660765ecbfd758843e45b9d4958ef8564f6301e074e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51034777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc54db08cc86fa877a2fe19ab641106ecd4fc39393a300021ea2371ab24735f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
ENV NODE_VERSION=22.11.0
# Tue, 29 Oct 2024 20:39:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="95e9a410b7ce732705493cd44496c8e77ccb11516c75c2ef794f19a9943d178c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENV YARN_VERSION=1.22.22
# Tue, 29 Oct 2024 20:39:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b7a1a9d97187d0d8e309cc79566d00ea7cb5a93172d5e5a9a2c01e75fd9f6`  
		Last Modified: Tue, 29 Oct 2024 23:23:19 GMT  
		Size: 46.7 MB (46719447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1005f7bb04e287e3dfb12577ae0c6b9bf3d6e885b9d230a2083cc03ad1fed2b`  
		Last Modified: Tue, 29 Oct 2024 23:23:17 GMT  
		Size: 1.4 MB (1387222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97076b5de13e29c0337f720f0c2b2dd3bc39c867757a2c0bee2819cf5b985bb8`  
		Last Modified: Tue, 29 Oct 2024 23:23:16 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:53e4b9009816b32da73de0864d14a8d9f05fd52cc951bcef96d9cecdb075491a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.7 KB (439680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134e32de88851855d47aadec1f529e1d7951cc323d3e8ed9ff48f26c6bbaa9c0`

```dockerfile
```

-	Layers:
	-	`sha256:a9a0af37faa11713c500a836e1f0f9cc709620113c89534b088f35dd8b8a97f5`  
		Last Modified: Tue, 29 Oct 2024 23:23:16 GMT  
		Size: 416.0 KB (415978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f596d2d99060b5d6f82ca1071db8023dd33d8581de56609c1199ab467781d7b8`  
		Last Modified: Tue, 29 Oct 2024 23:23:16 GMT  
		Size: 23.7 KB (23702 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull node@sha256:c828d05b851a52202b5e5f69d90b654f2fd5f0eb639411616e0120403d86bda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53341569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c9eda4655fc57f4104ee60190f7308c3b4ebbd443100d5e9de5a672529659f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
ENV NODE_VERSION=22.11.0
# Tue, 29 Oct 2024 20:39:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="95e9a410b7ce732705493cd44496c8e77ccb11516c75c2ef794f19a9943d178c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENV YARN_VERSION=1.22.22
# Tue, 29 Oct 2024 20:39:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29223bedee11d08c33ca41fe8328c83170ad1b82ee0039e83e488d4c7d38b40b`  
		Last Modified: Tue, 29 Oct 2024 22:42:27 GMT  
		Size: 48.6 MB (48594792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c3292f5b34b0e2986776e8098683fce58e3a726ff5340df2d5cf069f4370c`  
		Last Modified: Tue, 29 Oct 2024 22:42:26 GMT  
		Size: 1.4 MB (1387229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0960a5f3153b4d173ac1ae5f9a55d0ff99bc68b02f7a382aecaff7328a0549e`  
		Last Modified: Tue, 29 Oct 2024 22:42:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:4de345b790bf853ae577e0900f4b11336d3110ed1105e19375da2127cda5663b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.7 KB (439738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09cfd945e999d9054883a8086550f621f2a35c343d83d99f294dddb65ea3b32`

```dockerfile
```

-	Layers:
	-	`sha256:b4b9c14426d3721c36ce6780eb87ccae5600f69cca60181e6d5508b47ed9f4a0`  
		Last Modified: Tue, 29 Oct 2024 22:42:26 GMT  
		Size: 416.0 KB (416002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c510cd24d213b5dd3ad38ecf201fd0490ead7594b6157dc4c1c8e5d2bdaaec2`  
		Last Modified: Tue, 29 Oct 2024 22:42:26 GMT  
		Size: 23.7 KB (23736 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-alpine3.19` - linux; s390x

```console
$ docker pull node@sha256:97d401af89525308536fdff73e105ad1fd9fab01d95b1e072dc18063c1aec1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55299920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5ca2cabd45e7fd03892e59a7b4d00e1e9c5d5ba0039bc47bec644b9cbc7019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
ENV NODE_VERSION=22.11.0
# Tue, 29 Oct 2024 20:39:22 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         curl     && ARCH= OPENSSL_ARCH='linux*' && alpineArch="$(apk --print-arch)"       && case "${alpineArch##*-}" in         x86_64) ARCH='x64' CHECKSUM="95e9a410b7ce732705493cd44496c8e77ccb11516c75c2ef794f19a9943d178c" OPENSSL_ARCH=linux-x86_64;;         x86) OPENSSL_ARCH=linux-elf;;         aarch64) OPENSSL_ARCH=linux-aarch64;;         arm*) OPENSSL_ARCH=linux-armv4;;         ppc64le) OPENSSL_ARCH=linux-ppc64le;;         s390x) OPENSSL_ARCH=linux-s390x;;         *) ;;       esac   && if [ -n "${CHECKSUM}" ]; then     set -eu;     curl -fsSLO --compressed "https://unofficial-builds.nodejs.org/download/release/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz";     echo "$CHECKSUM  node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" | sha256sum -c -       && tar -xJf "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz" -C /usr/local --strip-components=1 --no-same-owner       && ln -s /usr/local/bin/node /usr/local/bin/nodejs;   else     echo "Building from source"     && apk add --no-cache --virtual .build-deps-full         binutils-gold         g++         gcc         gnupg         libgcc         linux-headers         make         python3         py-setuptools     && export GNUPGHOME="$(mktemp -d)"     && for key in       C0D6248439F1D5604AAFFB4021D900FFDB233756       DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7       CC68F5A3106FF448322E48ED27F5E38D5B0A215F       8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600       890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4       C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C       108F52B48DB57BB0CC439B2997B01419BD92F80A       A363A499291CBBC940DD62E41F10027AF002F8B0     ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;     done     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN) V=     && make install     && apk del .build-deps-full     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt;   fi   && rm -f "node-v$NODE_VERSION-linux-$ARCH-musl.tar.xz"   && find /usr/local/include/node/openssl/archs -mindepth 1 -maxdepth 1 ! -name "$OPENSSL_ARCH" -exec rm -rf {} \;   && apk del .build-deps   && node --version   && npm --version # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENV YARN_VERSION=1.22.22
# Tue, 29 Oct 2024 20:39:22 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 20:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 20:39:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c08c32e8c0a5d17ef84a6ed58a8a4ca0037ccb8a06b7806b5fcb52885defc7`  
		Last Modified: Tue, 29 Oct 2024 22:59:01 GMT  
		Size: 50.7 MB (50658912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8318d692e5a08e8f3229f49382edb5e639a4ed585ac30dde5f2830c9bd6c2e`  
		Last Modified: Tue, 29 Oct 2024 22:59:01 GMT  
		Size: 1.4 MB (1387206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c7fa13604362200194d325315974acc533521bd4238d63b994b27694a02130`  
		Last Modified: Tue, 29 Oct 2024 22:59:00 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-alpine3.19` - unknown; unknown

```console
$ docker pull node@sha256:3a6e18fc8dca01d72067d1f0a9c11e1ec9142c8748e730bc2b590bf3d4a47730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.6 KB (437591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44aab7685e64cf697285a98d5f9d43ccfcada8ae1c01f48a1821490c499728d`

```dockerfile
```

-	Layers:
	-	`sha256:18de79388cc5a4ff116b11ad1a12ec9bce37c1693ad4a922ae7ab536f4898c44`  
		Last Modified: Tue, 29 Oct 2024 22:59:01 GMT  
		Size: 414.0 KB (413980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcdf3fe615a13129f4e14c7dac22c4d34d78e862f627b422ccc253b4f06b992`  
		Last Modified: Tue, 29 Oct 2024 22:59:00 GMT  
		Size: 23.6 KB (23611 bytes)  
		MIME: application/vnd.in-toto+json
