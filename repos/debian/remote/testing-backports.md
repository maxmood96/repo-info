## `debian:testing-backports`

```console
$ docker pull debian@sha256:d26c1007dfcb4f068939f0ca8c4568751d4155090f27314b91c85b0641226800
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:31b210f1fe5aef60609e17642dcd4584e5814c2acdc4e86ee1d9894ffc7a3d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48758015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7231e1b973b3d0830185b3ab96cf93b8a4f0d9373a5c17307e1bbd165c9fd39`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:14:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:142f8d9fe96cbe7dc9590a27f0c94afed33e961d517f86e1e6dd218b76aaeea5`  
		Last Modified: Wed, 24 Jun 2026 00:28:26 GMT  
		Size: 48.8 MB (48757792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d657c44c986d96411d099f2d0064013c49484f1f959b8f693f08c0e39851599`  
		Last Modified: Wed, 24 Jun 2026 01:15:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7c4c51433c1ad8e33066770f837117d28c3f80b8efe25ae9498d4641b63c5948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b0d8d641141733ecef38a6fdbb5a161ec4de9bc259f0b01896545bc143c7d6`

```dockerfile
```

-	Layers:
	-	`sha256:624d27d542a9f0211f3aab41d35699a17233dec28743484d49f3ff6b57af3541`  
		Last Modified: Wed, 24 Jun 2026 01:15:03 GMT  
		Size: 3.2 MB (3150717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b04b1f84da73dd111a39c090f9eb65ccca194341d6690dd00bae1f25839a518`  
		Last Modified: Wed, 24 Jun 2026 01:15:03 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:30cfde65d1b3710668f37e352280ac81c00b7f9c51bec57ce81ad68f7d1505f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99c0de353ab4e47cf7969efb5027852e2680b682d338f99753433b92b8c997f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:15:22 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:17c8586e02588ff5c69ae25e8b2ed19f2efb6560f7d5a9b5037ca77d4d64729e`  
		Last Modified: Wed, 24 Jun 2026 00:28:32 GMT  
		Size: 45.7 MB (45653094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b7e733335cd6462309bf9f2a50d206ae945fdaeda574d82fc9a35692631754`  
		Last Modified: Wed, 24 Jun 2026 01:15:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c69c834bedffc1263267c1da7eb29de2095fd29b1b2a9d86dbbcc59c2863f6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617eac6c69d8db034531286068712e8044d82b11f17be201a6fde21ec07d03ac`

```dockerfile
```

-	Layers:
	-	`sha256:16f2fa83f9ee88f6d345a5aec8b163dab0030fc298f5da223ac53dc4a973056f`  
		Last Modified: Wed, 24 Jun 2026 01:15:29 GMT  
		Size: 3.2 MB (3152079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db53482096cf9a3701714b11ac5358ecbd50d0b51211e69c87d850b48adc6aa2`  
		Last Modified: Wed, 24 Jun 2026 01:15:28 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ba20d55399619e69e6c626376d91e7ed8e23d83c42e1ecd0999ec0a716a52057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48768935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4698b5bf74885f0f49d92f4bbfc0193b140957eae743def9757350aa194b68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:15:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2709552e86e8bfdf001e839c8a0a4aaf30f93a3eca6930cdf1a604c043c1b74c`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 48.8 MB (48768712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3838d1a5ba54cf2d9cf59c159c7128d5b84ea5eb40889b5526bd6d37192eb64e`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c44e2940df1a5bafd345618370f67fbd13132e6a76aa4d0708fee5158d8811dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e4c47f44b3e0842a950fd4f9b6bf3e303a32b908da4df9bf0a5050ca98fc9b`

```dockerfile
```

-	Layers:
	-	`sha256:0164064c90996e0e6e2c0661528c0723fdbcf238d91868bdb85d5d914c3ac9ec`  
		Last Modified: Wed, 24 Jun 2026 01:15:18 GMT  
		Size: 3.2 MB (3155387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e7e7e386e8144eb922e590b35ceda049588168d0a707d5fc886ed82c26e8cd2`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:44a8e750e64e6c092d5dc920602933f777f28932549c852746791d90f48fb670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50051257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237862a278d1cb8bbd94330f2e54b5918f17ea9ae1ef33423a2ad9f5891596be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:14:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:997fcd5cfd1d79c54a799ef1275b4e551794304b0dd4257811d1c2a741181727`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 50.1 MB (50051034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f07dccc220e57795fbe54b50dc0b4d0e1b957555679733b13f0aa6d5ff44952`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f89b8d34ce5cdcca3b5967918fdb89563530af93a59f58ddad27fc54a18fd6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797e6548f3c5db3ac737b3e7371c5bf8d11d6aeff05bed79016d3b2b7d14860b`

```dockerfile
```

-	Layers:
	-	`sha256:17c449d7a39b926faf20f5770df9b271eb92d7d45a009e9d1d5169ca4b516894`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 3.1 MB (3147921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d50ed9949bcb1bd2a6dec63f1fa0f7e6dcf753f7418844131559966800cddba`  
		Last Modified: Wed, 24 Jun 2026 01:14:50 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:28f9cf8f6e389fca943b8dc030ee10bffcc5ee157f82bf1370d224763513fbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54079253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17a96abd9457eab425c4196de9441582f506a5258776205a7d526b79163100`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:edc739abe003d71e29f51bd3f67a0748257a233f97beb886321f5f660e6cbaa8`  
		Last Modified: Wed, 24 Jun 2026 00:30:03 GMT  
		Size: 54.1 MB (54079031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fcc96aa82b7a61d2bf6c027af34cb9712953ca9cd5f4064f57346210c3c572`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9e775ce157ba50e6d0cf728694c504901d20a952d7da103855500c567df6b452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642d199c1045e9adfc190c9d7326aa17cfcafcf872a6b3314a7444bc81b7a4c8`

```dockerfile
```

-	Layers:
	-	`sha256:46bf505c03db0d03793eb2b886e767337fa5ca690897900a955622766eb4ab03`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 3.2 MB (3154214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54e5df05e5a6e355efa7a6fa1041f7a98856fce4086032318bbdf5b535da311`  
		Last Modified: Wed, 24 Jun 2026 01:15:17 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:1f21bfe1aa06420a5d2cb1c340af2ef1e2b3a048b495721e44ec8556627c66d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46847815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dc957f232b0848ac14b696f14e4de493ff013d70f83706fe02a746012c71b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 18:36:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5be0789409c0b2e3445ed499987310c85bc6fca646a07ca1121b30d91a16df7c`  
		Last Modified: Wed, 24 Jun 2026 03:36:29 GMT  
		Size: 46.8 MB (46847592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938fbbfa4bc10662fd43f4100045a4367f79b8a9c0c8aff6602d27a4a036d9da`  
		Last Modified: Wed, 24 Jun 2026 18:37:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fa6b37ecc1ca5b96a2d08f033b84cad5857fcb25c0fe8ed56fea748be2f71394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b2935152d6422d000ff92b1a51ad43d891628c2b6f87945e305b87ef3abdbd`

```dockerfile
```

-	Layers:
	-	`sha256:eb7578126db7e04305b1f97b1c77e9d7eaeb2a0899659b21655d21d46c7ddec6`  
		Last Modified: Wed, 24 Jun 2026 18:37:01 GMT  
		Size: 3.1 MB (3142217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa239fd33e38bd8a2d3e6d355fd79db658eaeb93dd1df4e92c303657704667b`  
		Last Modified: Wed, 24 Jun 2026 18:37:00 GMT  
		Size: 5.8 KB (5819 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:16cfe06192b515e2980303b37695cef3579478a8aaf37a7a391947d60de76435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48492061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92eb6e904483d37b01a5a49c904ea20cb50ea9a9ba07af11184fad20dc21b522`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1782172800'
# Wed, 24 Jun 2026 01:14:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:55f193d6691f14cc10d6580d69d5e9df4cd7390a771f2807ff18665a2262556f`  
		Last Modified: Wed, 24 Jun 2026 00:28:16 GMT  
		Size: 48.5 MB (48491840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd612fe16d38dacb644958cb75bc8689c2930162cb66a8e5cc083857162e4ca`  
		Last Modified: Wed, 24 Jun 2026 01:14:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f6f186f2ed267deb19398dd212cc4f59a11b3bb99335e085cb16708afe6bfff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205518027e61d2aa3b9eb1ba3ed96427f9cb9173c076003af91077ff5e66c4c4`

```dockerfile
```

-	Layers:
	-	`sha256:663de8de09173d08f6e3ee6db53d41dbe9681822caec674442f2ddcb4fb3cd36`  
		Last Modified: Wed, 24 Jun 2026 01:14:35 GMT  
		Size: 3.2 MB (3152168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1445b31fd8336cc3ec067be4f9e4cded583adfbf8f7a4e05aa92fda86202468f`  
		Last Modified: Wed, 24 Jun 2026 01:14:35 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
