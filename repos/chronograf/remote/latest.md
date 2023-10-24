## `chronograf:latest`

```console
$ docker pull chronograf@sha256:027250f8a0d951d6eb179f9aa95af5e48ae838828cd57475b028e121cd115f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:8707a48434c79a083a793fc3a00adbdefeaf5ff20280e62a3d9eb8b7cdc91867
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84100991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0183ad7dea3a08ef9c98258f292092257683dd86d7b727c4d20f5241f359aa47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:19:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:19:56 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:20:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:20:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:20:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:20:05 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:20:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:20:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:20:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a132e29de7276a64cd521d22645dc61b1bd2a4cb1a193ee49b92f93f0c2427`  
		Last Modified: Tue, 24 Oct 2023 00:20:41 GMT  
		Size: 7.9 MB (7873004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd741862bf739148be32c6ada53827d4813a14c883d4ded943726c667310019`  
		Last Modified: Tue, 24 Oct 2023 00:20:46 GMT  
		Size: 47.1 MB (47053724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133380af3438c8ba33b960dc9c75a0ef543bc8059af21d8317f731a5a400e4ed`  
		Last Modified: Tue, 24 Oct 2023 00:20:39 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1139951cabd1e82ec7779b81e70f07adc59c4ad9008db4f9c6169bf50c97d2e8`  
		Last Modified: Tue, 24 Oct 2023 00:20:39 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c9cd4aaebd28fe9606e68f451ffa4718326a40e21e3c947f887ad801d42f`  
		Last Modified: Tue, 24 Oct 2023 00:20:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f561842ea3ac1c45f50ae0d511db8fade073f7135618a809e6d934e166eefcb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75920594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95853d742a1a56e274165274664fe8b599273b187265f004ab759cbccbb436dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:57:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:57:28 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:57:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:57:39 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:57:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:57:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:57:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:57:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373ef288c1016255f23880fa193ed8c7b16d4316eb58a30fcd570f718deccd4`  
		Last Modified: Tue, 24 Oct 2023 00:57:55 GMT  
		Size: 6.5 MB (6497689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2639aee512dab0e2fe78d1a515ae90b96cc3d89f675da7730898afb2cf7a18`  
		Last Modified: Tue, 24 Oct 2023 00:58:00 GMT  
		Size: 44.6 MB (44649590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed879c5c9cd7cc45825042bf0c9e2eb2933605e0d70f4f07af5f3b304114cac2`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5b56f84fc2d127783ba14e5ded545ee284891285786a7e6a2ff86302561930`  
		Last Modified: Tue, 24 Oct 2023 00:57:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6392494cbb507a347e77034033f4d60c98c65638650c7b64bc988008353e0b3e`  
		Last Modified: Tue, 24 Oct 2023 00:57:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c9fe4efbd1d71455a6fa4b661b4d78e670d34f082c3d8b554c73d7e981f8addf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475822bc23d4a7a3706572d7590da773f63f34429209a46f4e6e787f9465543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Tue, 24 Oct 2023 00:39:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 24 Oct 2023 00:39:33 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 24 Oct 2023 00:39:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 24 Oct 2023 00:39:42 GMT
EXPOSE 8888
# Tue, 24 Oct 2023 00:39:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 24 Oct 2023 00:39:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 24 Oct 2023 00:39:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Oct 2023 00:39:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cdcc7908019036cf9c3d001ab98e52b489a56b0cf84628701cdd5171f58ba0`  
		Last Modified: Tue, 24 Oct 2023 00:39:59 GMT  
		Size: 7.7 MB (7650123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aa51a450f2913c77d18e427d6d96164c2512d6049b5deb2a55ac285fdf54bb`  
		Last Modified: Tue, 24 Oct 2023 00:40:04 GMT  
		Size: 44.8 MB (44773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf898ad709c1a0f6df7a3686c89f054fcc8c37cf07f5e6331b8fd90b996e3188`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcae01731a3dc25c2550dbbb256be4612a6daf965ea1a0a9e2f07357f994a5a8`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71d77cfe25f61f27d00798befe3934cd764f9d0e4af6328e313b3a86dd77c0`  
		Last Modified: Tue, 24 Oct 2023 00:39:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
