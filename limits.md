---
layout: default
title: ContextHVE
---

<div class="post">
	<h2 class="pageTitle">Video Editing Failure Cases Demos</h2>
	<p>Although our proposed model is able to retain the input conditions and generate high-quality edited videos naturally, it is not capable of performing well in certain scenarios.</p>
	<table border="0"> <!-- 表格边框设置为1 -->
	<tr> Case 1: Motion not aligned with relative position. This situation generally occurs when there is an overly dramatic change in the image while the action information is too small (character too small or action too small), leading to a mismatch between the content and the control conditions. </tr>
    <tr> <!-- 表格的一行 -->
        <th style="width: 456px;">Ground Truth</th> <!-- 表头单元格 -->
        <th style="width: 456px;">Pose</th> <!-- 表头单元格 -->
    </tr>
    <tr> <!-- 表格的一行 -->
        <th style="width: 456px;">Masked Scene</th> <!-- 表头单元格 -->
        <th style="width: 456px;">Ours</th> <!-- 表头单元格 -->
    </tr>
    </table>
	<table border="0"> <!-- 表格边框设置为1 -->
    <tr> <!-- 表格的另一行 -->
        <td> <!-- 表格的单元格 -->
            <video width="912" height="512" controls>
                <source src="/assets/img/fail/069505-clip_0000011002_gt_clip_0000011186_fg_crop.mp4" type="video/mp4">
                您的浏览器不支持视频标签。
            </video>
        </td>
    </tr>
</table>
	<table border="0"> <!-- 表格边框设置为1 -->
	<tr> Case 2: Foreground not aligned with original scene. This situation typically arises in scenarios where the differences between the reference figure and the input figure are too significant. For example, when the input figure is a full body, the model defaults to inserting a figure with a full body or nearly a full body into the corresponding mask area. However, when the original video's figure is a close-up or an upper body, it becomes difficult for the model to learn the significant transition in terms of the figure. This is because even though random occlusion and data augmentation are introduced during training, the stability of the pose localization and the ability to control the size of the character through the mask require the occlusion area to change minimally. Therefore, the insufficient generalization of the figure leads to a bad case where the reference figure is not directly generated from the pose. </tr>
    <tr> <!-- 表格的一行 -->
        <th style="width: 456px;">Ground Truth</th> <!-- 表头单元格 -->
        <th style="width: 456px;">Pose</th> <!-- 表头单元格 -->
    </tr>
    <tr> <!-- 表格的一行 -->
        <th style="width: 456px;">Masked Scene</th> <!-- 表头单元格 -->
        <th style="width: 456px;">Ours</th> <!-- 表头单元格 -->
    </tr>
    </table>
	<table border="0"> <!-- 表格边框设置为1 -->
    <tr> <!-- 表格的另一行 -->
        <td> <!-- 表格的单元格 -->
            <video width="912" height="512" controls>
                <source src="/assets/img/fail/069505-clip_0000011132_gt_clip_0000011168_fg_crop_pure.mp4" type="video/mp4">
                您的浏览器不支持视频标签。
            </video>
        </td>
    </tr>
</table>
	<table border="0"> <!-- 表格边框设置为1 -->
	<tr> Case 3: Foreground is too special to be compatible with the scene. </tr>
    <tr> <!-- 表格的一行 -->
        <th style="width: 456px;">Ground Truth</th> <!-- 表头单元格 -->
        <th style="width: 456px;">Pose</th> <!-- 表头单元格 -->
    </tr>
    <tr> <!-- 表格的一行 -->
        <th style="width: 456px;">Masked Scene</th> <!-- 表头单元格 -->
        <th style="width: 456px;">Ours</th> <!-- 表头单元格 -->
    </tr>
    </table>
	<table border="0"> <!-- 表格边框设置为1 -->
    <tr> <!-- 表格的另一行 -->
        <td> <!-- 表格的单元格 -->
            <video width="912" height="512" controls>
                <source src="/assets/img/fail/069505-clip_0000011192_gt_clip_0000011154_fg_crop.mp4" type="video/mp4">
                您的浏览器不支持视频标签。
            </video>
        </td>
    </tr>
</table>
</div>
