# Open Source Software Notices — StealthCap

**Version 1.0**

StealthCap (隐捕) is built on a number of open source libraries and frameworks. We thank the developers and communities of these projects for their contributions. The following notice lists the open source software distributed with StealthCap, together with their versions and licenses, in accordance with the applicable license obligations.

This notice applies unless otherwise stated. If any omission is found, please contact us so that it can be corrected.

## 1. Acknowledgments

StealthCap gratefully acknowledges and thanks the following open source projects for making their high-quality software available under open source licenses.

## 2. Third-Party Software

| Software | Version | License | Project Home |
|---|---|---|---|
| SkiaSharp | 3.119.4 | MIT License | https://github.com/mono/SkiaSharp |
| Skia (bundled native library via SkiaSharp) | as provided by SkiaSharp 3.119.4 | BSD 3-Clause License | https://skia.org/ |
| System.Security.Cryptography.ProtectedData | 9.0.0 | MIT License | https://github.com/dotnet/runtime |
| .NET Runtime (self-contained) | .NET 10 | MIT License | https://github.com/dotnet/runtime |
| Windows Forms (System.Windows.Forms) | .NET 10 | MIT License | https://github.com/dotnet/winforms |
| FFmpeg (bundled `ffmpeg.exe`) | git master N-126188-g426841da9d-20260817 | GPL-3.0 | https://ffmpeg.org/ |

### Notes

- **SkiaSharp** (MIT) is used for high-quality 2D graphics, image encoding and rendering.
- **Skia** is the native graphics engine that SkiaSharp binds to and is distributed alongside SkiaSharp as native binaries. It is licensed under the BSD 3-Clause License.
- **System.Security.Cryptography.ProtectedData** (MIT) is used to protect sensitive configuration data in the local Credential storage.
- The **.NET Runtime** and **Windows Forms** are statically bundled for a self-contained deployment. They are provided by the .NET Foundation under the MIT License.
- **FFmpeg**: StealthCap bundles a standalone `ffmpeg.exe` executable (git master build `N-126188-g426841da9d-20260817`) to export recordings to MP4. The bundled FFmpeg is a **GPL build** (configured with `--enable-gpl --enable-version3`, including GPL codecs such as libx264 and libx265) and is therefore licensed under the **GPL version 3**. StealthCap merely invokes `ffmpeg.exe` as a fully external, separate process via its command-line interface and does **not** link to, embed, or statically include any FFmpeg library in StealthCap's own binaries. Accordingly, the GPL obligations of FFmpeg do not apply to StealthCap's own proprietary code. The GPLv3 license text and the FFmpeg source code corresponding to the bundled build (available from https://ffmpeg.org / the official FFmpeg git repository at commit `426841da9d`) are provided, or offered in writing, with this distribution as required by the GPLv3.

## 3. License Texts

### 3.1 MIT License

The following software components are licensed under the MIT License:
SkiaSharp, System.Security.Cryptography.ProtectedData, .NET Runtime, Windows Forms.

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### 3.2 BSD 3-Clause License

The following software component is licensed under the BSD 3-Clause License: Skia.

> Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
>
> 1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
> 2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
> 3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
>
> THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

### 3.3 GNU General Public License version 3 (FFmpeg)

The bundled `ffmpeg.exe` is distributed under the GNU General Public License, version 3. The full text of the GPLv3 is shipped with this distribution under the filename `COPYING.gplv3`, in accordance with the GPLv3 requirement to provide a copy of the license. (If the license text file has been removed from your distribution package, please contact us and we will provide it.)

In accordance with GPLv3, the corresponding source code for the bundled FFmpeg build (commit `426841da9d`, version `N-126188-g426841da9d-20260817`) is available from the official FFmpeg git repository at https://git.ffmpeg.org/ffmpeg.git and from https://ffmpeg.org/download.html. StealthCap uses FFmpeg solely as an external command-line subprocess; no FFmpeg libraries are linked into StealthCap's proprietary binaries, and this notice does not impose GPL obligations on StealthCap's own code.

To the extent you desire a copy of the FFmpeg source code corresponding to the distributed binaries, it may be obtained free of charge by sending a written request via the contact information in the About page of StealthCap.

---

If you have any questions regarding this notice, please contact us via the "Contact Us" link in the About page of StealthCap.