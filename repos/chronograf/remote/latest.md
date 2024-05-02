## `chronograf:latest`

```console
$ docker pull chronograf@sha256:f8576295bb2633b50b8f2b3c8cc683708e74282cf1a768da80f45b1124de5ee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:2cb0b8b1da8690af36b9f7b4959bae0f25ba0a187424cac651b20650603445f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84060126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f0977dde354462ebac171186c995a845df807d021a0ac3ccdc47f42617d31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bca853186d9fa4f3d07e24de79741fa25427f0b2d0eab8996be63473fd1c48`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 7.7 MB (7676917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cc39eb1df3ab70aa7dacba37e772033cd108cd90bdaa74e45011d6198634e2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 47.2 MB (47208254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157983f1cb0f03e7a121bed8ff6e98027c8c6a3be7d161e4fe2b062522ec970`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f63d3959c98d650bf99c6413a0b9e85714a8cbcc9e7e258b319a70c5dbc23c3`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a815190e4fba0bf1463fe2293f2924dfdb71cff35211a1797c45aa66f62fb2`  
		Last Modified: Wed, 01 May 2024 21:52:27 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:1478d940f96dbaafe093d86241a298969ab344d11b536c0664e66d4e82608497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f85b25a662f4291186189dd5d3dc33534aa1725e52dcc65c37f9b2766cd1d97`

```dockerfile
```

-	Layers:
	-	`sha256:f54b34b309e82a1681005dc1777c2b0f8604c1d314cb797cfbd1505b30897ba4`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 2.7 MB (2655509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f8299d252d4df87db8af04601374b4348d6985c3594eb49c1877cdc524b51a`  
		Last Modified: Wed, 01 May 2024 21:52:26 GMT  
		Size: 16.1 KB (16052 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e7b87511934d274d44fdf7a810d210f8b2bebfedbca8c0de6128a5bda5f26532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75340418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44445870df96cde21c7fd5b24ea74b673c0850e9e01577c1b168553f9cef8453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50316fbdc37f48b441d6a5300c3b2f5011fe5ff93920de46d8e37f26b19c1d0c`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 6.3 MB (6301004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e807757725f3d1ccaff9e57a0166983a73816ed082c8ef4173e057c9c61e87`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 44.3 MB (44274487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dfb47a244cadf0ec10ec3b5b8d475fb580dac07af32b9a27dbcde94f0c3cd4`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff168616ff7f4d51eeab0e490b470d7be9bc49f74a5c75dd0769f58e6dd700d`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e9b69be2b29851b3a218eeb456c72de15f9662b211438a21f396067cd6a4a9`  
		Last Modified: Wed, 01 May 2024 22:09:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:25dc80c7fe7448e89953320590af015f568304748c3b4855343d6e9792d63195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc039a1ec77e176937bbd6406e7d5c07bd658a7893298e2a025947d0d09faef0`

```dockerfile
```

-	Layers:
	-	`sha256:b513cb3404b83faf32634e4946d2c0c5160a5001c8695d86ccfbb890a34cba61`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 2.7 MB (2657805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6e8b8f908a14cafee41c6387f290c5241c3caf12fa4e5a54d1a9694dcf7efb`  
		Last Modified: Wed, 01 May 2024 22:09:40 GMT  
		Size: 16.0 KB (15960 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:60a815700707f1df08df1029b83847eaa235f0e912a34fa6c253f12499024cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81636840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaf05222cf53da43f8ef2282da0792a02048e92364dbcd68d586504103b4409`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 13:23:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 13:23:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 26 Apr 2024 13:23:50 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 13:23:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Apr 2024 13:23:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 13:23:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb2e161aae97649675931a79d1973b601f753dd3f37c4532530c72c07636d3d`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 7.5 MB (7453129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130d13b51f5f0ed17ab174e642adb1112bb78775d279ad3c199e0b61bd90b9b`  
		Last Modified: Wed, 01 May 2024 22:27:06 GMT  
		Size: 45.0 MB (44979293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac52f1d1a62121ca7fcfe7cc928aade001f7b7874c8bd7b40e7256c5e3ea6e1a`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957a06817cfb183d334232ce4a1711d8735a39d983d25146bf657bf1f530254a`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 11.9 KB (11914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9bf80ee0ddb49a63ed6b1ca461f772f3c550d4d7c5615143ca62e3e21887ad`  
		Last Modified: Wed, 01 May 2024 22:27:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:f0e5abe681ea42d2efc7c7b8030e027274a57edf6ad0df5d93534ce2946ebdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f479d33da2a64ac7a34333ed6adc29193bb65bee2a716d94a348e2858f84a85`

```dockerfile
```

-	Layers:
	-	`sha256:7c4fdc79c78dae83df78d9db456f5b419479096350f7ddb60685cc893a76a462`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 2.7 MB (2655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032a014ac7dc76467dddff4fd025e78a13e66d45993577bb48911db0c688e710`  
		Last Modified: Wed, 01 May 2024 22:27:04 GMT  
		Size: 15.9 KB (15893 bytes)  
		MIME: application/vnd.in-toto+json
