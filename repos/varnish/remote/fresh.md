## `varnish:fresh`

```console
$ docker pull varnish@sha256:f0608bcfcfe658eafd2241d95dded61cc69bf955fb0e695a88ca4dee1d662b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:d4e2856f159f4c4cf380fb893cd36f4d6937205f29d62ec34453d8eea44cd99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122267345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd2d91023cd1c8273d3ce26b2185bffa2dd0f069f7e935d87e9e73745fd82e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:00 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:36:00 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:36:00 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:36:00 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:36:00 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:36:00 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:36:00 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:36:00 GMT
USER varnish
# Wed, 22 Apr 2026 01:36:00 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:36:00 GMT
CMD []
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601edb7781b9274ac218e7930845a6538310653cb711636fb099263596f2eefd`  
		Last Modified: Wed, 22 Apr 2026 01:36:14 GMT  
		Size: 92.5 MB (92484290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4de00aad0b69ff3b2f72326caaba6ad41c6a04f12cfa2122fddb510db7baa`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5241f96ed347e1a16d4c2dd38d9c05cd97a5b7df5bf5dccb0b878d3ef53f08d2`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afff8b7ee9ba14e5e92004e2887f23bbd72fd4c8812ad936c6997bb800ad083`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:0f867c8b714583d85915287708a1045ffc825382f0c7eb80797baec76f655d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc38cb393f19bd840c6efe114f940ef1a46984c21d55481be6ffc2d3248fb70`

```dockerfile
```

-	Layers:
	-	`sha256:85f810513181db83064f6da83400d25791193783208a0d85fd84e46477a169e5`  
		Last Modified: Wed, 22 Apr 2026 01:36:12 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:524b3a703e7fd2a5febff47a18e8c1e4c18b6b10e5231bf05cf52b19c6d70951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116258574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1949bf4e4687183b516beb39d13e89c5bd4ac5b44a00e95cd1a446fce4d47aa`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:46 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Wed, 22 Apr 2026 01:38:46 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Wed, 22 Apr 2026 01:38:46 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VARNISH_SIZE=100M
# Wed, 22 Apr 2026 01:38:46 GMT
ENV VSM_NOPID=1
# Wed, 22 Apr 2026 01:38:46 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
WORKDIR /etc/varnish
# Wed, 22 Apr 2026 01:38:46 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
COPY index.html /var/www/html/ # buildkit
# Wed, 22 Apr 2026 01:38:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Wed, 22 Apr 2026 01:38:46 GMT
USER varnish
# Wed, 22 Apr 2026 01:38:46 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Wed, 22 Apr 2026 01:38:46 GMT
CMD []
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51e88dbbba69d1c081d800c779001a16460d26a17170ac0a926d081e292c6a`  
		Last Modified: Wed, 22 Apr 2026 01:39:02 GMT  
		Size: 86.1 MB (86112080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac720f2cf45b018f15fa42faa7bf3de6f7e70e58ad120a611fba4206ec1570`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93078a388f3f282e7f7420d845ce957923734469a1862dea242eeea169aa9a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebf17e0159fd56e4d39430fbaf0dc5da21e0b7938aa5708aeaf1154024c742`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:e522aa6de935cab70ba77619d50c4fa66cd433443ed1dbba1231019b1a8729fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0e15384eb987ccfb5ba098e98cd04b6b153c719907962d33a0d0e1b4154a6b`

```dockerfile
```

-	Layers:
	-	`sha256:b0504082c9211a3de2803311791e2ccac9179ee556df15d8ccd8b04e5496181a`  
		Last Modified: Wed, 22 Apr 2026 01:38:57 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json
